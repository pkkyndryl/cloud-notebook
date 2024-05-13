# Summary of Cloud Providers Services
Last Updated: {{ git_revision_date_localized }}

[Another good, and similar resource that is helpful](https://comparecloud.in)

**Disclaimer: following 80/20 rule.... I'm focusing on top 80% of services**

| Domain | Purpose of the Service | Amazon Web Services | Google Cloud (GCP) | IBM Cloud   | Microsoft Azure|
| ---- |  ----- | ----- | ---- | ----- | ---- |
| **Foundations** |  |  |  |  |  |   
|  | Regions & Zones | [Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/?nc2=h_l2_cc) | [Regions and Zones](https://cloud.google.com/about/locations) | [Regions and Zones](https://cloud.ibm.com/docs/overview?topic=overview-locations) | [Regions](https://azure.microsoft.com/en-us/global-infrastructure/geographies/) |   
|  | Accounts | [Organizations](https://aws.amazon.com/organizations/) |  | [accounts](https://cloud.ibm.com/docs/account?topic=account-accounts) | [Resource Groups](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/manage-resource-groups-portal#what-is-a-resource-group) |  
|  | Industry certifications |  |  |  |  |   
|  | Vendor provided comparisons |  | [compare GCP to AWS](https://cloud.google.com/docs/compare/aws) |  | [compare Azure to GCP](https://cloud.google.com/docs/compare/azure) |   
|  | Support | [Support](https://aws.amazon.com/premiumsupport/) | [Support](https://cloud.google.com/support) |  | [Support](https://azure.microsoft.com/en-gb/support/plans/) |   
| **Cost Management** |  |  |  |  |  |   
|  | Pricing | [Cloud Services Pricing](https://aws.amazon.com/pricing/) | [Pricing](https://cloud.google.com/pricing/list) | [IBM Pricing](https://www.ibm.com/cloud/pricing) | [Pricing](https://azure.microsoft.com/en-us/pricing/calculator/) |   
|  | Pricing Calculator | [AWS calculator](https://calculator.s3.amazonaws.com/index.html) | [GCP Calculator](https://cloud.google.com/products/calculator) |  | [Pricing Calculator](https://azure.microsoft.com/en-us/pricing/calculator/) |   
|  | Cost Management | [Budgets]() | [Cost Management](https://cloud.google.com/cost-management) |  | [Cost Management](https://azure.microsoft.com/en-us/services/cost-management/) |   
|  |  |  |  |  |  |   
| **COMPUTE** |  |  |  |  |  |   
| Virtual Machines | Virtual Machines | [EC2](https://aws.amazon.com/ec2/?ec2-whats-new.sort-by=item.additionalFields.postDateTime&ec2-whats-new.sort-order=desc) | [Compute Engine](https://cloud.google.com/compute/) | [VSI](https://www.ibm.com/cloud/virtual-servers) | [Virtual Machines](https://azure.microsoft.com/en-us/services/virtual-machines/) |   
|  |  |  |   | [Virtual Servers](https://www.ibm.com/cloud/vpc) |  |   
|  | GPU Based VMs |  | [cloud GPUs](https://cloud.google.com/gpu) | [GPUs on IBM Cloud](https://www.ibm.com/cloud/gpu) | [GPU Optimized VMs)](https://azure.microsoft.com/en-us/pricing/details/virtual-machines/series/)    
|  |  |  | [Sole-Tenant Nodes](https://cloud.google.com/sole-tenant-nodes) | [Dedicated VMs](https://www.ibm.com/cloud/virtual-servers)  [Hyper Protect VM](https://cloud.ibm.com/docs/hp-virtual-servers?topic=hp-virtual-servers-getting-started) | [Dedicated Host](https://docs.microsoft.com/en-us/azure/virtual-machines/dedicated-hosts)    
| Containers |  |   |   |   |   |   
|   | Serverless Container hosting | [ECS](https://aws.amazon.com/ecs/) | [Cloud Run](https://cloud.google.com/run) |  | [Container Instances](https://azure.microsoft.com/en-us/services/container-instances/) |   
|  | Kubernetes Cluster service (CaaS) | [EKS](https://aws.amazon.com/eks/) | [Kubernetes Engine](https://cloud.google.com/kubernetes-engine) | [IKS](https://www.ibm.com/cloud/kubernetes-service) | [Azure Kubernetes Service](https://azure.microsoft.com/en-us/services/kubernetes-service/) |   
|  | RedHat OpenShift | [RedHat Openshift on AWS](https://aws.amazon.com/rosa/) |  | [ROKS](https://www.ibm.com/cloud/openshift) |  |   
|   | Serverless computing  | [Lambda](https://aws.amazon.com/lambda/) | [Cloud Functions](https://cloud.google.com/functions) | [Cloud Functions](https://www.ibm.com/cloud/functions)    | [Functions](https://azure.microsoft.com/en-us/services/functions/) |   
|  | serverless function orchestrator | [Step Functions](https://aws.amazon.com/step-functions/?step-functions.sort-by=item.additionalFields.postDateTime&step-functions.sort-order=desc) |  | [NodeRed]() |  |   
|  | Serverless computing - Container based | [Fargate](https://aws.amazon.com/fargate/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc&fargate-blogs.sort-by=item.additionalFields.createdDate&fargate-blogs.sort-order=desc) | [Cloud Run](https://cloud.google.com/run) | [Code Engine](https://cloud.ibm.com/codeengine/overview) |  |   
| App Hosting | PaaS | [Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/) | [App Engine](https://cloud.google.com/appengine) | [CloudFoundry](https://www.ibm.com/cloud/cloud-foundry) | [App Service](https://azure.microsoft.com/en-us/services/app-service/) |   
|  | Container Registry | [Elastic Container Registry](https://aws.amazon.com/ecr/) | [Container Registry](https://cloud.google.com/container-registry) | [IBM Container Registry](https://www.ibm.com/cloud/container-registry) |  [Container Registry](https://docs.microsoft.com/en-us/azure/container-registry/) |   
|  | Simplified app hosting | [Lightsail](https://aws.amazon.com/lightsail/) |  |  |   |   
|  | Auto Scaling Service | [Auto Scaling](https://aws.amazon.com/autoscaling/) |  | [Auto Scaling for VPC](https://cloud.ibm.com/docs/vpc?topic=vpc-creating-auto-scale-instance-group)  [classic autoscale](https://cloud.ibm.com/docs/virtual-servers?topic=virtual-servers-about-auto-scale) | [Virtual Machine Scale Sets](https://azure.microsoft.com/en-us/services/virtual-machine-scale-sets/) |   
|  | Hosted VMWare SDDC | [VMware Cloud on AWS](https://aws.amazon.com/vmware/) |  | [VMWare Cloud Service](https://www.ibm.com/cloud/vmware?p1=Search&p4=43700050328300451&p5=e&cm_mmc=Search_Google-_-1S_1S-_-WW_NA-_-ibm%20vmware_e&cm_mmca7=71700000060953359&cm_mmca8=aud-382859943522:kwd-83362848&cm_mmca9=CjwKCAiAgc-ABhA7EiwAjev-j-bI43H-QCb8EchaApVxcmsJfCUs7wdjAmRkt8dhw9kTODU-rkwAqBoC7hEQAvD_BwE&cm_mmca10=406208904362&cm_mmca11=e&gclid=CjwKCAiAgc-ABhA7EiwAjev-j-bI43H-QCb8EchaApVxcmsJfCUs7wdjAmRkt8dhw9kTODU-rkwAqBoC7hEQAvD_BwE&gclsrc=aw.ds) | [VMWare Solution](https://azure.microsoft.com/en-us/services/azure-vmware/) |   
|   | Batch processing/scheduling control service | [Batch](https://aws.amazon.com/batch/) |   |  | [Batch](https://azure.microsoft.com/en-us/services/batch/) |   
|  |  |  |  |  |  |   
| **STORAGE** |  |  |  |  |  |   
|  | Object Storage | [S3](https://aws.amazon.com/s3/) | [Cloud Storage](https://cloud.google.com/storage) | [Object Storage](https://www.googleadservices.com/pagead/aclk?sa=L&ai=DChcSEwjL0IDylcHuAhXNwMAKHTfZClgYABABGgJpbQ&ohost=www.google.com&cid=CAESQOD2DIgQX9jGeUYeUIMBrz5LuQ5-aHIkYvtJaF_vHSdn9a1Q113tSU_fXPDhfOAja5GilQ7nhFszXQMN243b-yU&sig=AOD64_1-kX5KuXCXKTMY5EmsFXe-0F4rPQ&q&adurl&ved=2ahUKEwjXnPfxlcHuAhXQU80KHZ9jAM4Q0Qx6BAgMEAE) | [Blob Storage](https://azure.microsoft.com/en-us/services/storage/blobs/) |   
|  | Block Storage | [EBS](https://aws.amazon.com/ebs/) | [Persistent Disk](https://cloud.google.com/persistent-disk) | [IBM Cloud Block Storage](https://www.ibm.com/cloud/block-storage) | [Managed Disks](https://azure.microsoft.com/en-us/services/storage/disks/) |   
|  | File Storage ( NFS) | [EFS](https://aws.amazon.com/efs/) | [FileStore](https://cloud.google.com/filestore) | [IBM Cloud File Storage](https://www.ibm.com/cloud/file-storage) | [File Storage](https://azure.microsoft.com/en-us/services/storage/files/) |   
|  | Archival Storage | [Glacier](https://aws.amazon.com/glacier/) | [Cloud Storage Archive](https://cloud.google.com/storage/archival) | [Object Storage](https://www.googleadservices.com/pagead/aclk?sa=L&ai=DChcSEwjL0IDylcHuAhXNwMAKHTfZClgYABABGgJpbQ&ohost=www.google.com&cid=CAESQOD2DIgQX9jGeUYeUIMBrz5LuQ5-aHIkYvtJaF_vHSdn9a1Q113tSU_fXPDhfOAja5GilQ7nhFszXQMN243b-yU&sig=AOD64_1-kX5KuXCXKTMY5EmsFXe-0F4rPQ&q&adurl&ved=2ahUKEwjXnPfxlcHuAhXQU80KHZ9jAM4Q0Qx6BAgMEAE) |  |   
|  | hybrid  | [Storage Gateway](https://aws.amazon.com/storagegateway/) |   |  | [StorSimple](https://azure.microsoft.com/en-us/services/storsimple/) |   
|  | Transfer to/from customers | [Snowball](https://aws.amazon.com/snowball/) | [Transfer Appliance](https://cloud.google.com/transfer-appliance/docs/4.0) | [Data Transfer Service](https://cloud.ibm.com/docs/DataTransferService?topic=DataTransferService-gettingstarted) | [Data Box](https://azure.microsoft.com/en-us/services/databox/) |   
|  |  | [Snowball Edge](https://aws.amazon.com/snowball/) |  | [Mass Data Migration](https://www.ibm.com/cloud/mass-data-migration) | [Data Lake Storage](https://azure.microsoft.com/en-us/services/storage/data-lake-storage/) |   
|  |  | [Snowmobile](https://aws.amazon.com/snowmobile/) |  |  |  |   
|  |  |  |  |  |  |   
| **NETWORKING** |  |  |  |  |  |   
| Virtual Private Cloud | core virtual network | [VPC](https://aws.amazon.com/vpc/) | [Virtual Private Cloud](https://cloud.google.com/vpc) | [VPC](https://cloud.ibm.com/docs/vpc?topic=vpc-getting-started) | [Virtual Network](https://azure.microsoft.com/en-us/services/virtual-network/)   - Vnets- |   
|  | network monitoring | [Flowlogs](https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html) |  | [Flowlogs](https://cloud.ibm.com/docs/vpc?topic=vpc-flow-logs) | [Network Watcher](https://docs.microsoft.com/en-us/azure/network-watcher/) |   
|  | peering | [VPC Peering](https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html) |  |  |  |   
|   | connecting with customer premise | [Direct Connect](https://aws.amazon.com/directconnect/) | [Cloud Interconnect](https://cloud.google.com/network-connectivity/docs/interconnect) | [DirectLink](https://www.ibm.com/cloud/direct-link) | [ExpressRoute](https://azure.microsoft.com/en-us/services/expressroute/) |   
|  | DNS | [Route 53](https://aws.amazon.com/route53/) | [CloudDNS](https://cloud.google.com/dns) | [DNS Services](https://www.ibm.com/cloud/dns) | [DNS](https://azure.microsoft.com/en-us/services/dns/) |   
|  | Connecting networks - gateway | [Transit Gateway](https://docs.aws.amazon.com/vpc/latest/tgw/what-is-transit-gateway.html) |  | [Transit Gateway](https://www.ibm.com/cloud/transit-gateway) |  |   
|  | application load balancing | [Application Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html) | [Cloud Load Balancing](https://cloud.google.com/load-balancing) | [VPC Load Balancing](https://www.ibm.com/cloud/load-balancer) | [Load Balancing](https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview) |   
|  |  | [Gateway Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html) |  |  |  |   
|  | Firewalls | [Network Firewall](https://docs.aws.amazon.com/network-firewall/) | [Firewall Rules](https://cloud.google.com/vpc/docs/firewalls) | [Firewall - Dedicated](https://cloud.ibm.com/docs/hardware-firewall-dedicated?topic=fortigate-10g-exploring-firewalls) | [Firewall](https://azure.microsoft.com/en-us/services/azure-firewall/)  ;  [Network Security groups](https://docs.microsoft.com/en-us/azure/virtual-network/network-security-groups-overview) |   
|  | Firewall Rule Mgmt | [Firewall Manager](https://docs.aws.amazon.com/firewall-manager/) |  |  |[Defender for Cloud](https://docs.microsoft.com/en-us/azure/defender-for-cloud/defender-for-cloud-introduction)  |   
|  |  | [Internet Gateway](https://docs.aws.amazon.com/network-firewall/) |  |  |  |   
|  |  | [Carrier Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/Carrier_Gateway.html) |  |  |  |   
|  | NAT Gateway | [NAT Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html) | [NAT Gateway](https://cloud.google.com/nat/docs/overview) |  | [Virtual Network NAT](https://docs.microsoft.com/en-us/azure/virtual-network/nat-overview) |   
|  | VPN Connections | [VPN Gateway](https://docs.aws.amazon.com/vpn/index.html) | [Cloud VPN](https://cloud.google.com/network-connectivity/docs/vpn/concepts/overview) | [VPN Gateway](https://cloud.ibm.com/docs/solution-tutorials?topic=solution-tutorials-vpc-site2site-vpn) | [VPN Gateway](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways) |   
|  |  | [Private Link](https://docs.aws.amazon.com/vpc/latest/userguide/Carrier_Gateway.html) |  |  |  |   
|   | Content Delivery Network | [CloudFront](https://aws.amazon.com/cloudfront/) | [Cloud CDN](https://cloud.google.com/cdn) | [IBM Cloud Internet Service](https://www.ibm.com/cloud/cloud-internet-services) | [CDN](https://azure.microsoft.com/en-us/services/cdn/) |   
|  |  |  |  |  |  |   
|  |  |  |  |  |  |   
| **DATABASE Services**     |  |  |  |   
| Relational/SQL Database | Relational DB | [RDS ](https://aws.amazon.com/rds/) | [Cloud SQL](https://cloud.google.com/sql) | [IBM Cloud Databases for  ](https://cloud.ibm.com/catalog?category=databases#services) | [SQL Database](https://azure.microsoft.com/en-us/services/sql-database/) |   
|  | MySQL/PostgreSQL | [Aurora](https://aws.amazon.com/rds/aurora/) | [Cloud Spanner](https://cloud.google.com/spanner) |  | [Database for MySQL](https://azure.microsoft.com/en-us/services/mysql/)  |   
|  | MongoDB | [Document DB]() | [FireStore](https://firebase.google.com/docs/firestore) | [IBM Cloud Databases for Mongo]() |   |   
|  |  |  |  |  | [Database for PostgreSQL](https://azure.microsoft.com/en-us/services/postgresql/) |   
| NoSQL Database | NoSQL key-value and document database | [DynamoDB](https://aws.amazon.com/dynamodb/) | [Cloud Bigtable](https://cloud.google.com/bigtable) | [IBM Cloud Databases for Mongo ](https://www.ibm.com/cloud/databases-for-mongodb) | [Cosmos DB](https://azure.microsoft.com/en-us/services/cosmos-db/) |   
|  | … |  | [Cloud Datastore](https://cloud.google.com/datastore) | [Cloudant](https://www.ibm.com/cloud/cloudant) |  |   
|  | HA NoSQL DB | [SimpleDB](https://aws.amazon.com/simpledb/) | [FireStore](https://firebase.google.com/docs/firestore) |  | [Table Storage](https://azure.microsoft.com/en-us/services/storage/tables/) |   
|  |  |  |  |  | [Data Warehouse](https://azure.microsoft.com/en-us/resources/videos/introduction-to-azure-sql-data-warehouse/) |   
|   | Data Warehouse Service | [RedShift](https://aws.amazon.com/redshift/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc) | [BigQuery](https://cloud.google.com/bigquery) |  |  |   
|   | In Memory Database | [Elasticache](https://aws.amazon.com/elasticache/) | [MemoryStore](https://cloud.google.com/memorystore) | [Databases for Redis](https://cloud.ibm.com/catalog/services/databases-for-redis) | [Redis Cache](https://azure.microsoft.com/en-us/services/cache/) |   
|  |  |  |  |  |  |   
| **PLATFORM Services** |  |  |  |  |  |   
|   | Message Queuing Service | [Simple Notification Service](https://aws.amazon.com/sns/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc) | [Pub/Sub](https://cloud.google.com/pubsub) | [Push Notifications](https://cloud.ibm.com/docs/mobilepush?topic=mobilepush-getting-started) | [Service Bus](https://docs.microsoft.com/en-us/azure/service-bus-messaging/service-bus-messaging-overview) |   
|   | BigData ( e.g. Hadoop) Services | [MapReduce](https://aws.amazon.com/emr/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc) | "[Dataproc](https://cloud.google.com/dataproc)  [Dataflow](https://cloud.google.com/dataflow)" | [Hadoop - 3rd party](https://cloud.ibm.com/catalog/content/hadoop-Qml0bmFtaS1oYWRvb3A=-global) | [HDInsight](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-overview) |   
|   | Stream based processing service | [Kinesis](https://aws.amazon.com/kinesis/) | [Pub/Sub](https://cloud.google.com/pubsub) | [Event Streams](https://www.ibm.com/cloud/event-streams) |  |   
|  | ETL Service | [glue](https://aws.amazon.com/glue/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc) |  |  |  |   
| Resiliency |  |  |  |  |  |   
|   | Archive and Backup | [Glacier](https://aws.amazon.com/glacier/) | [Cloud Storage Archive](https://cloud.google.com/storage/archival) | [Data Archiving](https://www.ibm.com/cloud/object-storage/data-archiving) | [Backup](https://azure.microsoft.com/en-us/services/backup/) |   
|   | Disaster Recovery Services |   |   |  | [Site Recovery](https://azure.microsoft.com/en-us/services/site-recovery/) |   
|  |  |  |  |  |  |   
|  |  |  |  |  |  |   
| **Security and Service Management** |  |  |  |  |  |   
| Authentication and Access Management | Identity and Access controls | [IAM](https://aws.amazon.com/iam/) | [Cloud IAM](https://cloud.google.com/iam) | [IAM](https://cloud.ibm.com/docs/account?topic=account-iamoverview) | [Active Directory](https://azure.microsoft.com/en-us/services/active-directory/)  ; [IAM](https://azure.microsoft.com/en-us/product-categories/identity/) |   
|  | Microsoft AD Service | [Directory Service](https://aws.amazon.com/directoryservice/) | [Managed Service for Microsoft AD](https://cloud.google.com/managed-microsoft-ad) |  | [Multi-Factor Authentication](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-mfa-howitworks) |   
|  | Cloud Account Management | [Organizations](https://aws.amazon.com/organizations/) |  | [IBM Cloud Enterprise Accounts](https://www.ibm.com/cloud/blog/announcements/introducing-ibm-cloud-enterprises) |  |   
|  | Single Signon | [Single Sign-On](https://aws.amazon.com/single-sign-on/) |   | [Single Sign On](https://cloud.ibm.com/docs/appid?topic=appid-cd-sso) |  |   
|  | Account/Organization Control Policies | [Service Control Policies](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html) |  |  |  |   
| Security |  |  |  |  |  |   
|   | Security information & Event Mgmt (SIEM)) |  |  |  | [Sentinel](https://docs.microsoft.com/en-us/azure/sentinel/overview) |   
|   | Threat Detection ( Continuous Security Monitoring) | [GuardDuty](https://aws.amazon.com/guardduty/) | [Cloud Event Threat Detection](https://cloud.google.com/event-threat-detection) | [Qradar on Cloud](https://www.ibm.com/products/hosted-security-intelligence) | [Security Center](https://azure.microsoft.com/en-us/services/security-center/) |   
|  | Security Operations Control Portal | [Security Hub](https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html) |  | [IBM Cloud Security Advisor](https://www.ibm.com/cloud/security-advisor) | [Defender for Cloud](https://docs.microsoft.com/en-us/azure/defender-for-cloud/defender-for-cloud-introduction) |   
|  | Manage data security & privacy | [Macie](https://aws.amazon.com/macie/) | [Cloud Security Scanner](https://cloud.google.com/security-command-center) |  |  |   
|  | Vulnerability Scanning | [Inspector](https://docs.aws.amazon.com/inspector/latest/userguide/inspector_introduction.html) | [Web Security Scanner](https://cloud.google.com/security-scanner/docs) |  |  |   
|  | DDoS Protection Service | [Shield](https://aws.amazon.com/shield/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc) | [Google Cloud Armor](https://cloud.google.com/armor) |  | [DDoS Protection](https://azure.microsoft.com/en-us/services/ddos-protection/) |   
|  | Web App Firewall | [WAF](https://aws.amazon.com/waf/) | [Google Cloud Armor](https://cloud.google.com/armor) | [IBM Cloud Internet Service](https://www.ibm.com/cloud/cloud-internet-services) | [Ddos Protection](https://docs.microsoft.com/en-us/azure/ddos-protection/ddos-protection-overview) ; [Web Application Firewall](https://azure.microsoft.com/en-us/services/web-application-firewall/) |   
|  | Investigate Root Cause of security findings | [Detective](https://docs.aws.amazon.com/detective/index.html) |  | [IBM Cloud Security Advisor](https://www.ibm.com/cloud/security-advisor) |  |   
|  |  |  |  |  |  |   
|  | Managing Secrets | [Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html?icmpid=docs_asm_console) | [Secret Manager](https://cloud.google.com/secret-manager) | [Secrets Manager](https://www.ibm.com/cloud/secrets-manager) | [Key Vault](https://azure.microsoft.com/en-us/services/key-vault/) |   
|  |  | [Audit Manager](https://docs.aws.amazon.com/audit-manager/latest/userguide/what-is.html) |  |  |  |   
|   | Key mgmt ( e.g. encryption keys) | [Key Mgmt Service](https://docs.aws.amazon.com/kms/) | [Cloud Key Management Service](https://cloud.google.com/kms) | [Key Protect](https://www.ibm.com/cloud/key-protect) |  |   
|  | Certificate mgmt | [Certificate Manager](https://docs.aws.amazon.com/acm/latest/userguide/acm-overview.html) |  | [Certificate Manager](https://www.ibm.com/cloud/certificate-manager)  |  |   
|  |  |  |  | [Cloud Data Shield](https://cloud.ibm.com/docs/data-shield) |  |   
|  |  |  |  |  |  |   
| Cloud Monitoring | Collect/Track metrics ( monitoring) | [CloudWatch](https://aws.amazon.com/cloudwatch/) | [Cloud Monitoring](https://cloud.google.com/monitoring) | [LogDNA](https://www.ibm.com/cloud/log-analysis) | [Application Insights](https://azure.microsoft.com/en-us/services/monitor/) |   
|  | Event History ( audit) | [CloudTrail](https://aws.amazon.com/cloudtrail/) | [Cloud Audit Logs](https://cloud.google.com/audit-logs) | [Activity Tracker with LogDNA](https://cloud.ibm.com/docs/containers?topic=containers-at_events) | [Log Analytics](https://azure.microsoft.com/en-us/services/monitor/) |   
|  | LogAggregation | [CloudWatch Logs](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html) | [Cloud Logging](https://cloud.google.com/logging) |  |  |   
| Cloud Management |  | [Systems Manager](https://aws.amazon.com/systems-manager/) | Stackdriver |  | [Portal](https://azure.microsoft.com/en-us/features/azure-portal/) |   
|  | Central Cloud portal/console | [Management Console](https://aws.amazon.com/console/) |  | [IBM Cloud Console](https://www.ibm.com/products/cloud-management-console) | [Policy](https://azure.microsoft.com/en-us/services/azure-policy/) |   
|  |  |  |  |  |  |   
| **DevOps** |  |  |  |  | [EventGrid](https://docs.microsoft.com/en-us/azure/event-grid/overview) |   
|  |  | [CodeStar](https://aws.amazon.com/codestar/) |   |  | [Visual Studio Team Services ](https://azure.microsoft.com/en-us/services/devops/) |   
|  |  | [CodePipeline](https://aws.amazon.com/codepipeline/) |  |  | [Visual Studio App Center](https://azure.microsoft.com/en-us/services/app-center/) |   
|   | Templates | [CloudFormation](https://aws.amazon.com/cloudformation/) | [Cloud Deployment Manager](https://cloud.google.com/deployment-manager) |  |  |   
|  | Asset Inventory & Configuration Management | [AWS Config](https://aws.amazon.com/config/) | [Cloud Asset Inventory](https://cloud.google.com/asset-inventory) |  |  |   
|  | continous deployment | CodeDeploy | Deploy |  | Pipeline |   
|  | collaborative Development | CodeCommit | Cloud Source Repository |  |  |   
|  | Continuous Builds | CodeBuild | Cloud Build |  |  |   
|  | container/serverless DevOps | [Proton](https://aws.amazon.com/proton/) |  |  |  |   
|  |  |  |  |  |  |   
| **SERVICES-AI** |  |  |  |  |  |   
|   | Machine learning tooling | [SageMaker](https://aws.amazon.com/sagemaker/) | Cloud Machine Learning Engine |  | Machine Learning |   
|  |  | [Apache MXNet on AWS](https://aws.amazon.com/mxnet/) |  |  |  |   
|  |  | [TensorFlow on AWS](https://aws.amazon.com/tensorflow/) |  |  |  |   
|  | Cognitive |  |  |  |  |   
|   | natural language processing | [Comprehend ](https://aws.amazon.com/comprehend/) | Cloud Natural Language  |  | Cognitive Services |   
|  | Conversational AI for Chatbots | [Lex](https://aws.amazon.com/lex/) | Cloud Speech API  |  |  |   
|  | text to speech | [Polly](https://aws.amazon.com/polly/) | Cloud Translation API  |  |  |   
|  | image and video analysis | [Rekognition](https://aws.amazon.com/rekognition/?blog-cards.sort-by=item.additionalFields.createdDate&blog-cards.sort-order=desc) | Cloud Video Intelligence |  |  |   
|  | language translation | [Translate](https://aws.amazon.com/translate/) |  |  |  |   
|  | speech to text | [Transcribe](https://aws.amazon.com/transcribe/) |  |  |  |   
|  | IoT |  |  |  |  |   
|   | connect IoT to cloud | [IoT Core](https://aws.amazon.com/iot-core/) | Cloud IoT Core |  | IoT Hub  |   
|  |  |  |  |  | IoT Edge |   
|  | Analytics |  |  |  |  |   
|   | interactive query analysis | [Athena](https://aws.amazon.com/athena/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc) | Cloud Dataflow  |  | HDInsight  |   
|  | bigdata platform | [EMR](https://aws.amazon.com/emr/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc) | Cloud Dataproc |  | Stream Analytics  |   
|  | real time streaming | [Kinesis](https://aws.amazon.com/emr/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc) |  |  | Data Lake Analytics  |   
|  |  |  |  |  | Analysis Services |   