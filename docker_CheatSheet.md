# Docker Cheat Sheet

Docker documentation: https://docs.docker.com/

**docker pull {IMAGE_NAME}** - Pull a container image directly from the Docker Hub.

**docker run {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine.

**docker run -it {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine in "*interative mode*".

**docker run --name {CONTAINER_NAME} {IMAGE_NAME}** - Run a container that will have a specific name.

**docker run -d {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine in "*detached mode*".

**docker run -d -P {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine in "*detached mode*" with an random outside port available.

**docker run -d -p {MACHINE_PORT}:{CONTAINER_PORT} {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine in "*detached mode*" with an outside port available.

**docker container ls** - Displays which containers are currently running.

**docker container rm $(docker container ls -aq)** - Remove all the containers on Docker.

**docker rmi $(docker image ls -aq)** - Remove all the images on Docker.

**docker container ls -a** - Displays the execution history of the containers present on the machine.

**docker container ls -s** - Displays the size of the running containers.

**docker stop {CONTAINER_ID}** - Stops the execution of the container itself and all its related internal processes.

**docker stop $(docker container ls -q)** - Stops all the containers in execution based on their IDs.

**docker start {CONTAINER_ID}** - Start the execution of the container itself and all its related internal processes.

**docker pause {CONTAINER_ID}** - Pauses the execution of the container itself and all its related internal processes. A paused container cannot be accessed.

**docker unpause {CONTAINER_ID}** - Unpauses the execution of the container itself and all its related internal processes.

**docker exec -it {CONTAINER_ID} {COMMAND}** - Execute the given container in "*interative mode*" running the given command. The container must already have been created.

**docker rm {CONTAINER_ID}** - Removes a container and all its contents.

**docker login -u {USERNAME)** - Login to Docker Hub.

**docker rm {CONTAINER_ID} --force** - Stops a container execution and removes it.

**docker port {CONTAINER_ID}** - Shows how the port mapping of a container is being done.

**docker images** - Shows all the images locally available for your Docker.

**docker image rm {IMAGE_ID}** - Delete a image from the local files.

**docker inspect {IMAGE_NAME OR IMAGE_ID}** - It demonstrates a lot of useful information about that image.

**docker history {IMAGE_NAME OR IMAGE_ID}** - It shows all the layers that make up that image and their respective information.

**docker build -t {IMAGE_NAME}:{VERSION} {DOCKERFILE_PATH}** - Create a new image based on the Dockerfile with the respective tags.

**docker tag {OLD_IMAGE_NAME}:{OLD_VERSION} {NEW_IMAGE_NAME}:{NEW_VERSION}** - Retag a local image.

**docker run -it --mount type=bind,source={LOCAL_PATH},target={CONTAINER_PATH} {IMAGE_NAME OR IMAGE_ID}** - Create a container with a "Bind Mount" volume.

**docker volume ls** - Shows the Volumes beign used in Docker.

**docker volume create {VOLUME_NAME}** - Create a new Volume to be used in Docker.

**docker volume inspect{VOLUME_NAME}** - Inspect the informations about a previously created Volume.

**docker run -it --mount source={VOLUME_NAME},target={CONTAINER_PATH} {IMAGE_NAME OR IMAGE_ID}** - Create a container with a "Volume" volume.

**docker run -it --mount type=tpmfs,target={CONTAINER_PATH} {IMAGE_NAME OR IMAGE_ID}** - Create a container with a "TMPFS" volume.

**docker network ls** - Show all the configurated networks using Docker.

**docker network create --driver bridge {NETWORK_NAME}** - Create a Docker network using "Bridge" drive.

**docker run -it --name {CONTAINER_NAME} --network {NETWORK_NAME} {IMAGE_NAME}** - Create a container with a specific name and using a previously created network.