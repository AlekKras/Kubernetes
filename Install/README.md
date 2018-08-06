# Configuration

There are four major installations:

- All-in-One Single-Node installation
- Single-Node etcd, Single-Master, and Multi-Worker installation
- Single-Node etcd, Multi-Master, and Multi-Worker installation
- Multi-Node etcd, Multi-Master, and Multi-Worker installation

# Localhost installation

- [Minikube](https://kubernetes.io/docs/getting-started-guides/minikube/)
- [Ubuntu on LXD](https://kubernetes.io/docs/getting-started-guides/ubuntu/local/)

# Tools to know

- [kubeadm](https://github.com/kubernetes/kubeadm) <br/>

kubeadm is a first-class citizen on the Kubernetes ecosystem. It is a secure and recommended way to bootstrap the Kubernetes cluster. It has a set of building blocks to setup the cluster, but it is easily extendable to add more functionality. Please note that kubeadm does not support the provisioning of machines.

- [KubeSpray](https://github.com/kubernetes-incubator/kubespray) <br/>

With KubeSpray (formerly known as Kargo), we can install Highly Available Kubernetes clusters on AWS, GCE, Azure, OpenStack, or bare metal. KubeSpray is based on Ansible, and is available on most Linux distributions. It is a Kubernetes Incubator project.

- [Kops](https://github.com/kubernetes/kops) <br/>

With Kops, we can create, destroy, upgrade, and maintain production-grade, highly-available Kubernetes clusters from the command line. It can provision the machines as well. Currently, AWS is officially supported. Support for GCE and VMware vSphere are in alpha stage, and other platforms are planned for the future.
