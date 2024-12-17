
FROM nginx:alpine-slim


# OCI lables
LABEL org.opencontainers.image.authors="schrodinger404"
LABEL org.opencontainers.image.title="looking at RUN & EXPOSE"
LABEL org.opencontainers.image.description="A Nginx application."
LABEL org.opencontainers.image.version="1.0"
LABEL org.opencontainers.image.created="2024-12-17"
LABEL org.opencontainers.image.url="https://github.com/schrodinger404/docker/tree/main/login-page-docker"


# Copy all Nginx configuration files from nginx-conf directory
COPY nginx-conf/*.conf /etc/nginx/conf.d/

# Copy all HTML files from nginx-html directory
COPY nginx-html/*.html /usr/share/nginx/html/

# Install curl using RUN
RUN apk --no-cache add curl

# Expose the ports 8081, 8082, 8083 (default port 80 already exposed from base nginx image)
EXPOSE 8081 8082 8083