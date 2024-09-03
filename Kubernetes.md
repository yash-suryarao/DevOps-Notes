## Kubernetes Architecture

In the K8s architecture there are 2 types of nodes __Master node (Control Plane)__ and __Worker Node (Worker Plane)__

• __Master node:__
Master node also known as Control Plane is responsible for managing the K8s cluster. It controls the scheduling, scaling and overall lifecycle of the containers of worker nodes. and it contains 4 components:

__1. API Server:-__ API server act as a central control point. API server helps to communicate between control plane and worker plane whenever the pod get restart or removed API server communicate with worker node to create new pods.

__3. Scheduler:-__ Scheduler are responsible for assigning pods to worker nodes. The scheduler determines which Node are valid placement for each pod in the scheduling queue based on resource availability.

__4. Controller Manager:-__ The controller Manager monitors the current state of cluster through API server and makes appropriate changes to keep the application running by ensuring sufficient Pods are in a healthy state.
<br>`Types of Controller Manager= DeamonSet, Deployment, Service, Statefulset, and Node Controller.`

__5. etcd:-__ etcd is database of k8s server that store metadata/action that perform by the objects present in worker node and master node (kubelet, scheduler, API server, controller manager) in form of key-value pair.


• __Worker node:__
Worker node is virtual or physical machine, that depending on the K8s cluster. It responsible for executing containerized application inside pod. Each worker node contains services necessary to run pods. worker node are managed by Control plane.
There are 4 components in the worker node. 

__1. Pods:-__ Pods are smallest deployable units in the K8s cluster and the pod can hold one or more containers. A single Worker Node can have more than one pods or it can have a single pod as well.

__3. Kubelet:-__ The kubelet is the agent running on worker node. It communicates with the master node and manages the pods. The kubelet ensures that the desired state of the containers, as defined by the master node. As well Kubelet monitors the lifecycle of pods which helps to start and stop the pods.

__4. Container Runtime:-__ The container runtime, such as Docker Engine, is responsible for pulling container images from a registry and running them as containers on the worker node. It provides the infrastructure that allows containers to run.

__5. Kube Proxy:-__ Kube Proxy is used for pod to pod communication, load balancing and network proxying. It make the application accessible to the end users.
Kube proxy manages networking for pods it allocate IP and ports to the pods.


## Pods
