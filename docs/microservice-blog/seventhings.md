# So what? Why now?

__Original blog publish date: May 23, 2015__

In my previous posts I’ve looked into the past on this topic and some of the fundamentals of what constitutes a microservices architecture. However, as a consultant and an architect I often find myself asking “So what? Why is this coming up again, especially since it is not new and has encountered challenges in the past?”

Upon reflection I think there are 7 key things that make it relevant to look at this now. I’ll touch on these for now and cover more completely later.

### API economy:
The movement to exposing and consuming Apis in the simple to use REST approach has been key in my mind to reopening the possibilities for a micro services architecture. Now, using the standard REST APIs, combined with the revel ant use of XML and JSON message formats, architects are enabled with a simpler way to publish and call the functionality of micro services.

In addition , when API gateways are employed, the ability to version and put a facade in front of the published API calls increases the loose coupling and maintain ability of such an architecture.

### Containers and container based packaging:
This is a big one because now there is a “standard” way to package up a microservice , application, runtime, OS, etc... Into a nicely deplorable unit. The fact the definition of this container ( e.g, Docker Container) can be managed as code using something like a Dockerfile and versioned also is an enabler of flexible deployment capabilities.

Containers also are an enabler of “divide and conquer” in that they allow each micro service team to design, build, test, and even deploy their work using the language and run times that best suits there needs.

### Templates and automated configuration management technology:
One challenge with a microservices architecture is that inn the end you have a lot of Lego blocks that are ” cute” by themselves, but they do need to be able to be structured and managed as a solution.

This is where technologies such as OpenStack Heat templates and DSLs such as Chef and Puppet come into play. The use of a Heat template can allow the orchestrated deployment of a set of containers ( e.g. Microservices) and supporting runtimes, such as API Gateways. By linking the template to specific Chef recipes , we now have a way to automatically modify and tune the configuration of the contents of the container, if needed, to support specific application needs. Either during deployment or while the environment is running.

Templates and recipes also provide repeatability to a microservices architecture. Since there can be a number of pieces, mistakes can easily be made during deployment.

### Cloud technologies and Autoscaling on the cloud:
Ok, this is a big one. The simplicity and flexibility to stand up IaaS quickly, via. APIs, is key to the renewed interest in microservices architectures. Just ask Netflix, Facebook, etc.. The ability to deploy services ( and servers ) globally, without human intervention , and have transactions routed to the specific APIs really opens up possibilities.

The cloud provider Autoscaling capabilities ( e.g. AWS or IBM SoftLayer) also becomes a key enabler of scaling a microservices architecture.Cloud based container support is also a key enabler. As cloud providers offer container runtimes to host Docker Containers, it will become even easier to quickly deploy microservices containers and get them running at global scale. This is why AWS has introduced a container service to its EC2 environment and IBM has added Docker Container support to its Bluemix offerings.

### Movement to NoSQL and the “polyglot” of languages
One of the challenges I had early on designing solutions like this with Forte’ was a) you were constricted by the language, and b) you had to deal with relational databases, and those pesky data architects. ( can you tell I was an object oriented architect ?)

The emergence of NoSQL technology and JSON opens up new ways to think about persistence. I’ll be covering that more in a post later.

Regarding “b” above, for those of you with a workshop you know it is nice to have multiple tools in your workshop. Well, software development is the same. You want to use the right tool. Now that the world as embraced the use of multiple languages and runtimes ( python, ruby, nodejs/JavaScript, java ) ...combined with container deployment, the flexibility and ability to go free has increased multiple fold.

### Internet of Things technologies and approaches:
This may seem out of place but I reference it for one key item. A microservices architecture needs a control layer to help knit the various APIs together. The use of IoT technologies such as NodeRed enables this in an open source manner. As this post is getting long I’ll cover this in more detail later too.

### DevOps
Finally, DevOps. Yes this does seem like a buzzword filled post. But where combines the continuous delivery capabilities enabled by DevOps processes and tools, combined with everything else referenced above, you now have the ability to automatically continuously improve and enhance a solutions developed using a microservices architecture, without a full scale upgrade or rip and replace.

Obviously, there have been other advancements since I wrote the paper referenced in my first post, but I think these are key. Moving forward I’ll pick up a deeper dive into some of the challenges crafting a micro services architecture using these technologies.