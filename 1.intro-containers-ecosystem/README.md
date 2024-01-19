# Introduction and Overview of Containers

# Sumário:

# Containers:

## What is?
- In computing, a container is an encapsulated process that includes the required runtime dependencies for the program to run.

- In a container, application-specific libraries are independent of the host operating system libraries, and the ones that are not specific to the containerized application are provided by the operating system and kernel.

- A container engine creates a union file system by merging container image layers. Because container image layers are immutable, a container engine adds a writable layer for runtime file modifications.

- Containers are ephemeral by default, which means that the container engine removes the writable layer when you remove the container.

## How it operates?
- Containers use Linux kernel features, such as namespaces and Control Groups (cgroups).
    - Containers use cgroups for resource management, such as CPU time allocation and system memory. 
    - Namespaces in particular provide the functionality to isolate processes within containers from each other and from the host system.
- Most container engines conform to the [OCI](https://opencontainers.org/) specifications, so developers can confidently build their deployable target artifacts to run as OCI containers.

- Containers can be split into two similar but distinct ideas: container images and container instances.
    - A container image contains effectively immutable data that defines an application and its libraries.
    - You can use container images to create container instances, which are executable versions of the image that include references to networking, disks, and other runtime necessities.
    - You can use a single container image multiple times to create many distinct container instances. You can also run these instances across multiple hosts. The application within a container is independent of the host environment.

# Kubernetes:
- The smallest manageable unit in Kubernetes is a **pod**, which represents a single application and consists of one or more containers, including storage resources and an IP address.

- Kubernetes **clusters** provide a modern container platform that addresses the concerns and challenges of running applications at scale. No matter the deployment size, Kubernetes implementations deliver a robust infrastructure and ease of management.

- Use container images to create container instances. 

- Container instances are executable versions of the image, and include references to networking, disks, and other runtime necessities.

# Podman
- Podman is a container engine to build and run containers on an individual host.

# Redhat RHOCP
- Kubernetes and Red Hat OpenShift Container Platform (RHOCP) orchestrate containers across multiple hosts called **nodes**.

- RHOCP is a set of modular components and services that are built on top of Kubernetes to add capabilities for the following features:
    - Remote management

    - Multiple tenants

    - Increased security

    - Continuous integration

    - Continuous development

