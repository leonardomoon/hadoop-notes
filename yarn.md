# Yet Another Resource Negotiator

## Anatomy of a YARN Application Run:
- YARN provides its core services via 2 types of long running daemons:
    - a resouce manager (one per cluster): manage the use of resource across cluster
    - node managers running on all the nodes in the cluster to launch and monitor containers. A container executes an application-specific process with a constrained set of resources (CPU, memory, etc)

- To run an application on YARN:
    - a client contacts the resource manager and asks it to run an application master process
    - the resource manager then finds a node manager that can launch the application master in a container
