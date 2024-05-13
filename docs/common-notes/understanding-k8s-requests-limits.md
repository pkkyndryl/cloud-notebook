# Understanding Requests and Limits in K8S


### Because there has been ongoing confusion, I’m providing this summary:

1. When deploying Containers to Kubernetes (K8S) you can specify “Requests” and “Limits” on virtual CPUs and RAM ( memory )
2. Kubernetes uses this information to determine which node ( worker node ) to deploy the pod/container onto AND when to eject it for “bad behavior”
3. A “Request” is a guaranteed reservation. This is what the Kubernetes Scheduler uses to determine where to put the container.
4. A “Limit” is the max amount the system will allow the container to use.

### Hence:

- If the value you specify for the “Request” is equal to the “Limit” then you are guaranteed the Limit about.
- If the “Request” is less than the “Limit” then, you are guaranteed the amount you requested, and IF your container starts to consume more, Kubernetes will “scavenge” your request UP TO THE LIMIT from what is available on the node.  In essence, you are grabbing resources others may need.
- [updated] Now... remember this all influences where Kubernetes runs you pod/container. Typically, Kubernetes has many worker nodes supporting a cluster. Therefore, if the K8S scheduler can't fit/run your container on one worker node, it will look for others in the cluster it can run on. Of course, the flexibility it has depends on affinity rules that have been setup for the pod/container.

### Therefore:

- Test your app to make sure you have a good profile of what the “Requested” amount needs to be and the max (“Limit”) you think will be needed.
- Don’t set Request == Limit unless you KNOW you need that.  This will block others AND increase costs.
- Sizing of Clusters will NOT be based on Limits

### Think of it this way…

- We are running an airline.  When you deploy your containers with Resource “requests” and “limits” you are providing information to us, the airline.
- If you feel you need 5 seats, for sure, then you set your “Request” to 5.    We, the airline, will guarantee those seats.
- If you think that you may have 10 other people coming, in addition to the 5, then you set your “Limit” to 15.
- Now,  when you show up at the gate with 8 people, we, the airline, will TRY to seat the other 3 IF there are available seats.  If they are not they may not be seated.
- I.e. Think of it this way.. OVERBOOKING a plane
- [updated] And remember.... Airlines usually have more than one plane. So, while the 3 additional members of your party can't fit on the same plane, they could go on other planes. (Building on the K8S approach above... the Airline will book all 8 people in your party on a plane with capacity.)

## Supporting information

* [Googles View](https://cloud.google.com/blog/products/containers-kubernetes/kubernetes-best-practices-resource-requests-and-limits)
* [Kubernetes View](https://learnk8s.io/setting-cpu-memory-limits-requests)
