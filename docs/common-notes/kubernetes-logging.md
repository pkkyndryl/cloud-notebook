# Notes regarding logging in Kubernetes

Because this keeps coming up, and I needed a common place to put these notes, I'm creating this page. This is a *work in progress* and currently reflects information relative to IBM Cloud, but I'll be modifying this shortly as I connect the dots to other cloud providers.

I do need to validate that this is consistent across cloud providers.

- Gary

---

### Common Capabilities required:

- Infrastructure level
    - Capture
        - Ability to capture log files generated by the compute infrastructure: VMs, Containers, Hypervisors, Kubernetes
        - Ability to capture log files generated by the network infrastructure: e.g. VMWare NSX and cloud VPC flow logs, including firewalls, load balancers, WAF, etc…
        - Ability to capture log files generated by database services and storage services
        - Ability to capture log files related to security auditing. These audit level log files need to be captured by various sources sent to a SEIM tool
    - Aggregation & Management
        - Ability to aggregate log files captured from various infrastructure environments into a single repository for searching and analysis.
        - Ability to aggregate log files globally, regionally, or by country as requirements dictate
        - Ability to rotate and archive log files to manage space and performance
    - Viewing and Search
        - Ability to search infrastructure level logs for messages related to a specific environment, or geography
        - Ability to search infrastructure level logs for messages of a specific type
        - Ability to search infrastructure level logs for messages by a period of time
        - Ability to search infrastructure level logs associated to a specific application running on the infrastructure
        - Ability to control access to the type and level of log files that can be searched/viewed.
        - Ability to give application DevOps teams access to infrastructure log files.
- Application level
    - Capture
        - Ability to capture log messages created by an application when the application writes to stdout/stderr. i.e. managed by syslog infrastructure
        - Ability to capture log messages created by an application when the application writes to log files it creates. i.e. not stdout
        - Ability to capture application audit level log messages
    - Aggregation & Management
        - Ability to aggregate all application centric log files together to facilitate analysis
        - Ability to rotate and archive log files to manage space and performance
    - Viewing And Search
        - Ability for application developers to have access to application level log files to aid analysis/debugging.
        - Ability for application DevOps teams to have access to application log files to aid analysis/debugging.
        - Ability to search for application level audit messages
- Supporting Information
    - https://pages.github.kyndryl.net/multicloud/mcmp-deployment-architecture/monitoring/logging/
    - https://w3.ibm.com/ocean/w3publisher/ibm-cloud-did-you-know
- Solution Approaches
    - Cloud service agents/plugins forwarding logs from K8S and VMs to cloud monitoring

### Key Points in how Logging Works in Kubernetes:

1. When the code, running a container, in a K8S pod writes to syslog ( e.g. `syslog()` ) , the actual log entry is stored in a file, associated to the container instance. The file is located in /var/log/containers on the worker node OS.
1. Agents, running on the worker node in containers or at the OS level, can then forward the logs to an external service.
1. _more to come_

___What is logged___

This information is leveraging content [located here](https://cloud.ibm.com/docs/containers?topic=containers-health#configuring). While this is referencing IBM Cloud, the approach is similar to how other cloud providers work.

1. Worker nodes ( OS Level )
    - worker: Information that is specific to the infrastructure configuration that you have for your worker node.
    - Worker logs are captured in syslog and contain operating system events.
        - /var/log/syslog
    - In auth.log you can find information on the authentication requests that are made to the OS.  
        - /var/log/auth.log
2. Containers running on the worker nodes
    - container: Information that is logged by a running container. Anything that is written to STDOUT or STDERR.
    - EACH container instance has it’s own log file.
        - /var/log/containers
3. Applications
    - application: Information about events that occur at the application level. This could be a notification that an event took place such as a successful login, a warning about storage, or other operations that can be performed at the app level.
        - Paths: You can set the paths that your logs are forwarded to. However, in order for logs to be sent, you must use an absolute path in your logging configuration or the logs cannot be read. If your path is mounted to your worker node, it might have created a symlink. Example: If the specified path is /usr/local/spark/work/app-0546/0/stderr but the logs actually go to /usr/local/spark-1.0-hadoop-1.2/work/app-0546/0/stderr, then the logs cannot be read.
4. Persistent storage
    - storage: Information about persistent storage that is set up in your cluster. Storage logs can help you set up problem determination dashboards and alerts as part of your DevOps pipeline and production releases. Note: The paths /var/log/kubelet.log and /var/log/syslog also contain storage logs, but logs from these paths are collected by the kubernetes and worker log sources.
        - Paths:
            - /var/log/ibmc-s3fs.log
            - /var/log/ibmc-block.log
        - Pods:
            - portworx-***
            - ibmcloud-block-storage-attacher-***
            - ibmcloud-block-storage-driver-***
            - ibmcloud-block-storage-plugin-***
            - ibmcloud-object-storage-plugin-***
5. Kube-system namespace
    - kubernetes: Information from the kubelet, the kube-proxy, and other Kubernetes events that happen in the kube-system namespace of the worker node. These can be sent to LogDNA.
    - Paths:
        - /var/log/kubelet.log
        - /var/log/kube-proxy.log
        - /var/log/event-exporter/1..log
6. Kubernetes api
    * kube-audit: Information about cluster-related actions that is sent to the Kubernetes API server, including the time, the user, and the affected resource.
7. Application load balancer
    - ingress: Information about the network traffic that comes into a cluster through the Ingress ALB.
    - Paths:
        - /var/log/alb/ids/*.log
        - /var/log/alb/ids/*.err
        - /var/log/alb/customerlogs/*.log
        - /var/log/alb/customerlogs/*.err