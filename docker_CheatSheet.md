# Docker Cheat Sheet

Docker documentation: https://docs.docker.com/

**docker pull {IMAGE_NAME}** - Pull a container image directly from the Docker Hub.

**docker run {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine.

**docker run -it {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine in "*interative mode*".

**docker run -d {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine in "*detached mode*".

**docker run -d -P {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine in "*detached mode*" with an random outside port available.

**docker run -d -p {MACHINE_PORT}:{CONTAINER_PORT} {IMAGE_NAME}** - Run a container available locally, or in DockerHub, on the machine in "*detached mode*" with an 
outside port available.

**docker container ls** - Displays which containers are currently running.

**docker container ls -a** - Displays the execution history of the containers present on the machine.

**docker stop {CONTAINER_ID}** - Stops the execution of the container itself and all its related internal processes.

**docker stop $(docker container ls -q)** - Stops all the containers in execution based on their IDs.

**docker start {CONTAINER_ID}** - Start the execution of the container itself and all its related internal processes.

**docker pause {CONTAINER_ID}** - Pauses the execution of the container itself and all its related internal processes. A paused container cannot be accessed.

**docker unpause {CONTAINER_ID}** - Unpauses the execution of the container itself and all its related internal processes.

**docker exec -it {CONTAINER_ID} {COMMAND}** - Execute the given container in "*interative mode*" running the given command. The container must already have been 
created.

**docker rm {CONTAINER_ID}** - Removes a container and all its contents.

**docker login -u {USERNAME)** - Login to Docker Hub.

**docker rm {CONTAINER_ID} --force** - Stops a container execution and removes it.

**docker port {CONTAINER_ID}** - Shows how the port mapping of a container is being done.

**docker images** - Shows all the images locally available for your Docker.

**docker image rm {IMAGE_ID}** - Delete a image from the local files.

**docker inspect {IMAGE_NAME OR IMAGE_ID}** - It demonstrates a lot of useful information about that image.

**docker history {IMAGE_NNAME OR IMAGE_ID}** - It shows all the layers that make up that image and their respective information.

**docker build -t {IMAGE_NAME}:{VERSION} {DOCKERFILE_PATH}** - Create a new image based on the Dockerfile with the respective tags.

**docker tag {OLD_IMAGE_NAME}:{OLD_VERSION} {NEW_IMAGE_NAME}:{NEW_VERSION}** - Retag a local image.
