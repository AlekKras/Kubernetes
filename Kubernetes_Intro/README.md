# What is Kubernetes?

According to <a href="https://kubernetes.io/">Kubernetes wesite</a>:

> "Kubernetes is an open-source system for automating deployment, scaling,
> and management of containerized applications."

**Kubernetes** comes from the Greek word **κυβερνήτης:**, which means helmsman or ship pilot. With this analogy in mind, we can think of Kubernetes as the manager for shipping containers.

Kubernetes is also referred to as **k8s**, as there are 8 characters between k and s.

Kubernetes is highly inspired by the Google Borg system, which we will explore in this chapter. It is an open source project written in the Go language, and licensed under the Apache License Version 2.0.

Kubernetes was started by Google and, with its v1.0 release in July 2015, Google donated it to the Cloud Native Computing Foundation (CNCF). We will talk more about CNCF later in this chapter.

Generally, Kubernetes has new releases every three months.

# Kubernetes Features

- **Automatic binpacking**

Kubernetes automatically schedules the containers based on resource usage and constraints, without sacrificing the availability.

- **Self-healing**

Kubernetes automatically replaces and reschedules the containers from failed nodes. It also kills and restarts the containers which do not respond to health checks, based on existing rules/policy.

- **Horizontal scaling**

Kubernetes can automatically scale applications based on resource usage like CPU and memory. In some cases, it also supports dynamic scaling based on customer metrics.

- **Service discovery and Load Balancing**

Kubernetes groups sets of containers and refers to them via a Domain Name System (DNS). This DNS is also called a Kubernetes service. Kubernetes can discover these services automatically, and load-balance requests between containers of a given service.

- ** Automated rollouts and rollbacks**

Kubernetes can roll out and roll back new versions/configurations of an application, without introducing any downtime.

- **Secrets and configuration management**

Kubernetes can manage secrets and configuration details for an application without re-building the respective images. With secrets, we can share confidential information to our application without exposing it to the stack configuration, like on GitHub.

- **Storage Orchestration**

With Kubernetes and its plugins, we can automatically mount local, external, and storage solutions to the containers in a seamless manner, based on software-defined storage (SDS).

- **Batch exdcution**

Besides long running jobs, Kubernetes also supports batch execution.
