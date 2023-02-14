# Alura Docker

Docker project, created as part of the online training "Docker: Criando e Gerenciando Contêineres" from @alura-challenges, an online school for coding and software development. 
The objective of this repository is serve as a knowledge library for me (@chiachio-pedro) while learning some new software development stuff...

## What is Docker?

Problems that Docker solves:

- Port conflict.
- Change versions in a practical way.
- Control of memory and cpu resources.
- Simplified maintenance process.

Similar to a virtual machine generated through a Hypervisor layer, which will have an isolated OS. And what is the advantage of Docker? Docker will be able to run 
multiple isolated applications through containers, without having to simulate a new OS.

Why are containers lighter?

While a virtual machine simulates the operating system as a whole, containers operate as if they were processes, so their consumption is lower than that of a virtual 
machine.

How do containers ensure isolation?

In order to guarantee the isolation of a container in an operating system, they operate through the concept of "Namespaces":

- PID: Provides for isolation of processes operating within a container.
- NET: Provides for the isolation of network interfaces.
- IPC: Provides for isolation of communication between processes and shared memory.
- MNT: Provisions for isolation of filesystem/mount points.
- UTS: Provides kernel isolation. Acting as if the container were another host.

How do containers work without an OS?

Through the aforementioned "Namespace", the UTS, the container is able to isolate a part of the Kernel that will only be used for that process, so the native OS of the 
machine has an isolated part of the system as a whole that will act as the container's OS.

How do containers manage system resources?

Just as "Namespaces" are responsible for isolating the container in the operating system, there is another concept responsible for managing the allocation of resources 
in each container, the "CGroups".

## Usage: 

For the Docker container to work, it needs an image, an image that can be found locally or through Docker Hub.

Main steps:

- Reproduce Docker image from a locally made file struct or by cloning a repository.
- Build the Docker image locally.
- Start a new container based on the Docker image built in the last step.
- Share that container through Docker Hub.

NOTE: Docker containers are only running as they perform some task, if the task is terminated the container will also be terminated.

Docker execution flow:

Searches for the image locally -> Downloads the image if not found locally -> Validates the image hash -> Runs the container.

What is a "hash"?

Hash is a mathematical function that converts a file of any size into a fixed length code of letters and numbers. This data representation ends up serving as the 
file's "fingerprint".
