
FROM nginx:alpine-slim


# OCI lables
LABEL org.opencontainers.image.authors="schrodinger404"
LABEL org.opencontainers.image.title="login"
LABEL org.opencontainers.image.description="A Nginx application."
LABEL org.opencontainers.image.version="1.0"
LABEL org.opencontainers.image.created="2024-12-17"
LABEL org.opencontainers.image.url="https://github.com/schrodinger404/docker/tree/main/login-page-docker"


# copy content to the docker image from local machine
COPY index.html styles.css /usr/share/nginx/html/

# ADD provides the additional features (readme)

# ADD <tar.gz, archives from the URL, etc..>