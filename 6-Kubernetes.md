## 1. What is Container Orchestration
`Container orchestration is the automation of much of the operational effort required to run containerized workloads and services.` This includes a wide range of things software teams need to manage a container's lifecycle, including provisioning, deployment, scaling (up and down), networking, load balancing and more.

## 2. What is Kubernetes
Kubernetes is an open-source container orchestration tool for automating software deployment, scaling, and management containerized applications.

## Kubernetes Architecture
<img src="https://miro.medium.com/v2/resize:fit:828/format:webp/0*fOP7i8w794bWvUuM.png">

### Worker Node (Worker Plane):
A Node is a `worker machine in Kubernetes and may be either a virtual or a physical machine, depending on the cluster.` Each Node is managed by the control plane. A Node can have multiple pods, and the Kubernetes control plane automatically handles scheduling the pods across the Nodes in the cluster.

__1. Pod:-__ Pods are smallest deployable units in the Kubernetes cluster and the pod can hold one or more containers. A single worker node can have one or more than one pods.

__2. Kubelet:-__ The kubelet is the `agent` running on each `worker node`. It communicates with the master node and manages the containers running on the node. The kubelet ensures that the `desired state` of the `containers`, as defined by the master node, is maintained.

__3. Container Runtime:-__ The container runtime, such as Docker, is responsible for pulling container images from a registry and running them as containers on the worker node. It provides the underlying infrastructure that allows containers to function.

__4. Kube Proxy:-__ Kube Proxy is responsible for network proxying, pod-to-pod communication and load balancing. It enables communication between services and pods by routing network traffic to the appropriate destination, ensuring connectivity within the cluster.

### Master Node (Controle Plane):
The master node is `responsible for cluster management and for providing the API that is used to configure and manage resources within the Kubernetes cluster.` Kubernetes master node components can be run within Kubernetes itself, as a set of containers within a dedicated pod.

__1. API Server:-__ 

__2. Scheduler:-__ 

__3. Controller Manager:-__ 

__4. etcd:-__ 
