# docker
learning docker

# to pull the docker image
List Docker images
docker images

Pull Docker image from Docker Hub
docker pull schrodinger404/login:v1

Alternatively, pull from GitHub Packages (no download limits)
docker pull ghcr.io/stacksimplify/mynginx:v1

# Run the downloaded docker images
Run Docker Container
docker run --name <CONTAINER-NAME> -p <HOST_PORT>:<CONTAINER_PORT> -d <IMAGE_NAME>:<TAG>

Example using Docker Hub image:
docker run --name mylogin -p 8080:80 -d schrodinger404/login:v1

Or using GitHub Packages image:
docker run --name mylogin -p 8080:80 -d ghcr.io/stacksimplify/mynginx:v1


# List running containers
List only running containers
docker ps

List all containers (including stopped ones)
docker ps -a

List only container IDs
docker ps -q

Connect to docker container
docker exec -it mylogin /bin/sh

Inside the container, you can run commands:
ls
hostname
exit  # To exit the container's terminal

# Stop, Start docker containers
Stop a running container
docker stop <CONTAINER-NAME>

Example:
docker stop mylogin

Start the stopped container
docker start <CONTAINER-NAME>

Example:
docker start myapp1

Verify the container is running
docker ps

# Remove docker containers
Stop the container if it's still running
docker stop <CONTAINER-NAME>
docker stop mylogin

Remove the container
docker rm <CONTAINER-NAME>
docker rm mylogin

stop and remove the container in one command
docker rm -f <CONTAINER-NAME>
docker rm -f mylogin

# Remove images
List Docker images
docker images

Remove Docker image using Image ID
docker rmi <IMAGE-ID>

Example:
docker rmi ad1234def

Remove Docker image using Image Name and Tag
docker rmi <IMAGE-NAME>:<IMAGE-TAG>

Example:
docker rmi schrodinger404/mylogin:v1