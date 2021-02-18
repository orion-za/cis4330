### Why use virtual machines?

One advantage of virtual machines is that they allow for more efficient use of computing power. When using physical machines alone, some of their power may go unused. With virtual machines you can put this “stranded capacity” to use by deploying machines that use exactly as much computing power as they need.

Virtual machines also allow for greater isolation of applications. On a physical machine, one application might end up using resources required by another application. With virtual machines applications can’t access anything beyond their virtual environment, thus protecting resources.

Virtual machines can be beneficial for organizational and logistical purposes. Different departments can all share physical machines if they have their own virtual machines. They also allow for upgrades and patches to system software to be scheduled as needed for the individual machines rather than all at once. They are quick to deploy and destroy, so they reduce the overhead of setting up new systems. This can all be automated since virtual machines are programmable.

### Why use containers?

Containers are like very small, stripped down virtual machines. As a result they are less wasteful than VMs can be. They are very lightweight because unlike VMs they don’t require an operating system; containers only have the programs they need. They provide isolation like VMs do but at a significant reduced cost. Memory and storage space is allocated dynamically for containers, unlike VMs which must have resources allocated head of time and may not use all of them.

Each container has its own copy of the libraries, packages, and other shared files that it needs. They are not affected by the dependencies of other containers which eliminates dependency-related problems that can occur on a machine where, for instance, one program requires a certain version of a dependency and another program requires a different one.

### Why use physical machines?

Physical machines are reliable and predictable since they depend on hardware to operate rather than a network of shared resources. As such they are appropriate for systems where failure is costly or even dangerous, such as transportation.

### Microservices and the cloud

Microservices and the cloud go well together because they reduce the cost of scaling and deploying. This matters when you are using cloud services because you pay for the resources you use. Microservices can save you money on the cloud by making scaling and deployment more efficient.

On the other hand, microservices can lead to increased complexity because they adopt the stack that is most suited for them. This can be difficult to manage on your own infrastructure, but using cloud services can help because they manage the infrastructure for you.
