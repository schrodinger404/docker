### Build docker image
```
# Build the Docker image
docker build -t <IMAGE_NAME>:<TAG> .

# Example:
docker build -t login:v1 .

# List Docker images
docker images

# Run the Docker container and verify
docker run --name <CONTAINER-NAME> -p <HOST_PORT>:<CONTAINER_PORT> -d <IMAGE_NAME>:<TAG>

# Example:
docker run --name mylogin -p 8090:80 -d login:v1

# Access the application in your browser
http://localhost:8090
```

### Push the docker image
```
# List Docker images
docker images

# Tag the Docker image
docker tag login:v1 schrodinger404/login:v1


# Push Docker image to Docker Hub
docker push schrodinger404/login:v1

```