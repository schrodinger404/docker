## EXPOSE & RUN

### Build and Run
```
# Build image
E:\docker\expose-docker>docker build -t expose-run:v1 .

# Image built
E:\docker\expose-docker>docker images
REPOSITORY   TAG       IMAGE ID       CREATED         SIZE
expose-run   v1        0a0a24acd35f   6 minutes ago   22.7MB

# verify lables with image ID
E:\docker\expose-docker>docker inspect 0a0a24acd

# Running container with multiple ports to expose diferent htmls at ports
E:\docker\expose-docker>docker run --name run-expose-cont -p 8080:80 -p 8081:8081 -p 8082:8082 -p 8083:8083 -d expose-run:v1

# Container
E:\docker\expose-docker>docker ps
CONTAINER ID   IMAGE           COMMAND                  CREATED         STATUS         PORTS                                                    NAMES
9153d91b18f9   expose-run:v1   "/docker-entrypoint.…"   3 minutes ago   Up 3 minutes   0.0.0.0:8081-8083->8081-8083/tcp, 0.0.0.0:8080->80/tcp   run-expose-cont


```
### Login to container 
```

E:\docker\expose-docker>docker exec -it 9153d91b1 ls /etc/nginx/conf.d
default.conf     nginx-8081.conf  nginx-8082.conf  nginx-8083.conf


E:\docker\expose-docker>docker exec -it 9153d91b1 ls /usr/share/nginx/html
50x.html         index-8081.html  index-8082.html  index-8083.html  index.html

E:\docker\expose-docker>docker exec -it 9153d91b1 ls /usr/share/nginx/html

# inside the Container
curl http://localhost
curl http://localhost:8081
curl http://localhost:8082
curl http://localhost:8083

# Exit
exit

```

