## 1. What is Container Orchestration
`Container orchestration is the automation of much of the operational effort required to run containerized workloads and services.` This includes a wide range of things software teams need to manage a container's lifecycle, including provisioning, deployment, scaling (up and down), networking, load balancing and more.

## 2. What is Kubernetes
Kubernetes is an open-source container orchestration tool for automating software deployment, scaling, and management containerized applications.

## Kubernetes Architecture
<img src="https://miro.medium.com/v2/resize:fit:828/format:webp/0*fOP7i8w794bWvUuM.png">

In the Kubernetes architecture there are two types of nodes Master Node (Control plane) and Worker Node (Worker plane):

### Master Node (Controle Plane):
Master node also known as `Control Plane` is responsible for managing the K8s cluster. It controls the `scheduling, scaling and overall lifecycle` of the containers of worker nodes. There are 4 components in Master Node:

__1. API Server:-__ API server act as a central control point. API server helps to communicate between control plane and worker plane whenever the pod get restart or removed API server communicate with worker node to create new pods.

__2. Scheduler:-__ Scheduler are responsible for assigning pods to worker nodes. The scheduler determines which Node are valid placement for each pod in the scheduling queue based on resource availability.

__3. Controller Manager:-__ The controller Manager monitors the current state of cluster through API server and makes appropriate changes to keep the application running by ensuring sufficient Pods are in a healthy state.
**Types of Controller Manager= DeamonSet, Deployment, Service, Statefulset, and Node Controller.

__4. etcd:-__ etcd is database of k8s server that store metadata/action that perform by the objects present in worker node and master node (kubelet, scheduler, API server, controller manager) in form of key-value pair.


### Worker Node (Worker Plane):
`A Worker Node is a virtual or a physical machine, depending on the K8s cluster.` Each Node is managed by the control plane. A Node can have multiple pods, and the Kubernetes control plane automatically handles scheduling the pods across the Nodes in the cluster.

There are 4 components in the worker node.
__1. Pod:-__ Pods are smallest deployable units in the Kubernetes cluster and the pod can hold one or more containers. A single worker node can have one or more than one pods.

__2. Kubelet:-__ The kubelet is the `agent` running on each `worker node`. It communicates with the master node and manages the pods running on the node. The kubelet ensures that the `desired state` of the `containers`, as defined by the master node, is maintained. As well kubelete monitors the lifecycle of pods which helps to start and stop the pods.

__3. Container Runtime:-__ The container runtime, such as Docker, is responsible for pulling container images from a registry and running them as containers on the worker node. It provides the underlying infrastructure that allows containers to function.

__4. Kube Proxy:-__ Kube Proxy is responsible for network proxying, pod-to-pod communication and load balancing. It enables communication between services and pods by routing network traffic to the appropriate destination, ensuring connectivity within the cluster.
