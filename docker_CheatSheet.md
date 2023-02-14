# Docker Cheat Sheet

**docker pull {IMAGE_NAME}** - Pull a container image directly from the Docker Hub.
**docker run {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine.
**docker run -it {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine in "*interative mode*".
**docker run -d {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine in "*detached mode*".
**docker run -d -P {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine in "*detached mode*" with an random outside port available.
**docker run -d -p {MACHINE_PORT}:{CONTAINER_PORT} {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine in "*detached mode*" with an outside port available.
**docker container ls** - Displays which containers are currently running.
**docker container ls -a** - Displays the execution history of the containers present on the machine.
**docker stop {CONTAINER_ID}** - Stops the execution of the container itself and all its related internal processes.
**docker start {CONTAINER_ID}** - Start the execution of the container itself and all its related internal processes.
**docker pause {CONTAINER_ID}** - Pauses the execution of the container itself and all its related internal processes. A paused container cannot be accessed.
**docker unpause {CONTAINER_ID}** - Unpauses the execution of the container itself and all its related internal processes.
**docker exec -it {CONTAINER_ID} {COMMAND}** - Execute the given container in "*interative mode*" running the given command. The container must already have been created.
**docker rm {CONTAINER_ID}** - Removes a container and all its contents.
**docker rm {CONTAINER_ID} --force** - Stops a container execution and removes it.
**docker port {CONTAINER_ID}** - Shows how the port mapping of a container is being done.
