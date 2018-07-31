# What are containers?

<b>Containers</b> are an application-centric way to deliver high-performing, scalable applications on the infrastructure of your choice.

With a <b>container image</b>, we bundle the application along with its runtime and dependencies. We use that image to create an isolated executable environment, also known as container. We can deploy containers from a given image on the platform of our choice, such as desktops, VMs, cloud, etc.

# What is Container Orchestration?

In the *quality assurance (QA) environments*, we can get away with running containers on a single host to develop and test applications. However, when we go to production, we do not have the same liberty, as we need to ensure that our applications:

* Are fault-tolerant
* Can scale, and do this on-demand
* Use resources optimally
* Can discover other applications automatically, and communicate with each other
* Are accessible from the external world
* Can update/rollback without any downtime.


*Container orchestrators* are the tools which group hosts together to form a cluster, and help us fulfill the requirements mentioned above.

# Container Orchestrators

There are many:

* <a href="https://docs.docker.com/engine/swarm/">Docker Swarm</a>

* <a href="https://kubernetes.io">Kubernetes</a>

* <a href="https://github.com/mesosphere/marathon">Mesos Marathon </a>

* <a href="https://aws.amazon.com/ecs/">Amazon ECS </a>

* <a href="https://www.nomadproject.io">Hashicorp Nomad</a>

# Why use Container Orchestrators?

Container orchestrators can:

* Bring multiple hosts together and make them part of a cluster
* Schedule containers to run on different hosts
* Help containers running on one host reach out to containers running on other hosts in the cluster
* Bind containers and storage
* Bind containers of similar type to a higher-level construct, like services, so we don't have to deal with individual containers
* Keep resource usage in-check, and optimize it when necessary
* Allow secure access to applications running inside containers.

# Where to deploy Container Orchestrators?

Most container orchestrators can be deployed on the infrastructure of our choice. We can deploy them on bare metal, VMs, on-premise, or on a cloud of our choice. For example, Kubernetes can be deployed on our laptop/workstation, inside a company's datacenter, on AWS, on OpenStack, etc. There are even one-click installers available to set up Kubernetes on the cloud, like Google Kubernetes Engine on Google Cloud, or Azure Container Service on Microsoft Azure. Similar solutions are available for other container orchestrators, as well
