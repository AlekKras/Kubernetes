# Arhitecture

At a high level, Kubernetes has the following main components:

- Master nodes
- Worked nodes
- Distributed key-value stor, like **etcd**

![Image of Architecture](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/8f441b27101be805bc286e67adc671a2/asset-v1:LinuxFoundationX+LFS158x+1T2018+type@asset+block/Kubernetes_Architecture1.png)

# Master nodes

Master node is responsible for managing the Kubernetes cluster, and it is the entry point for all administrative tasks. We can communicate to the master node via the CLI, the GUI (Dashboard), or via APIs.

![Master Node](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/2511418094dc96ba81800ad199feec9c/asset-v1:LinuxFoundationX+LFS158x+1T2018+type@asset+block/Master_Node1.png)

For fault tolerance purposes, there can be more than one master node in the cluster. If we have more than one master node, they would be in a HA (High Availability) mode, and only one of them will be the leader, performing all the operations. The rest of the master nodes would be followers.

To manage the cluster state, Kubernetes uses etcd, and all master nodes connect to it. etcd is a distributed key-value store, which we will discuss in a little bit. The key-value store can be part of the master node. It can also be configured externally, in which case, the master nodes would connect to it.

## Master Node Components

- API Server
- Scheduler
- Controller manager
- etcd

## Mater Node Components: API Server

All the administrative tasks are performed via the API server within the master node. A user/operator sends REST commands to the API server, which then validates and processes the requests. After executing the requests, the resulting state of the cluster is stored in the distributed key-value store.

## Master Node Components: Scheduler

As the name suggests, the scheduler schedules the work to different worker nodes. The scheduler has the resource usage information for each worker node. It also knows about the constraints that users/operators may have set, such as scheduling work on a node that has the label disk==ssd set. Before scheduling the work, the scheduler also takes into account the quality of the service requirements, data locality, affinity, anti-affinity, etc. The scheduler schedules the work in terms of Pods and Services.

## Master Node Components: Controller manager

The controller manager manages different non-terminating control loops, which regulate the state of the Kubernetes cluster. Each one of these control loops knows about the desired state of the objects it manages, and watches their current state through the API server. In a control loop, if the current state of the objects it manages does not meet the desired state, then the control loop takes corrective steps to make sure that the current state is the same as the desired state.

## Master Node Components: etcd

As discussed earlier, etcd is a distributed key-value store which is used to store the cluster state. It can be part of the Kubernetes Master, or, it can be configured externally, in which case, master nodes would connect to it.

# Worker Node

A worker node is a machine (VM, physical server, etc.) which runs the applications using Pods and is controlled by the master node. Pods are scheduled on the worker nodes, which have the necessary tools to run and connect them. A Pod is the scheduling unit in Kubernetes. It is a logical collection of one or more containers which are always scheduled together

![Worker Mode](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/cca459b616974dca1face4a7a14808e7/asset-v1:LinuxFoundationX+LFS158x+1T2018+type@asset+block/Worker_Node.png)

## Worker Node Components

- Container runtime
- kubelet
- kube-proxy

## Worker Node Components: Container runtime

- [containerd](https://containerd.io/)
-
