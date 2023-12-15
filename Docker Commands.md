# Docker Commands Classification and Usage

This is a **CheatSheet** README.md file that provides information on the classification and detailed usage of common **Docker commands**.


## What is Docker?

**Docker** is a platform that enables developers to automate the deployment of applications inside lightweight, portable containers. A container packages an application and its dependencies together, ensuring consistency across different environments. Unlike traditional virtualization, Docker containers share the host operating system's kernel, making them more efficient and lightweight.

## Why Use Docker?

- **Portability:** Containers encapsulate applications and their dependencies, ensuring consistent behavior across various environments.
  
- **Isolation:** Containers provide process isolation, allowing applications to run independently without interfering with each other.

- **Efficiency:** Docker containers share the host OS kernel, reducing resource overhead compared to traditional virtualization.

- **Scalability:** Docker enables easy scaling of applications, allowing developers to replicate and distribute containers effortlessly.

- **DevOps Integration:** Docker facilitates a DevOps approach, streamlining collaboration between development and operations teams.

- **Microservices Architecture:** Docker is well-suited for microservices, enabling the development and deployment of modular, independently deployable services.


## Table of Contents
1. [Container Lifecycle Management Commands](#1-docker-run-run-a-container)
2. [Image Management Commands](#2-docker-build-build-an-image)
3. [List and Inspection Commands](#4-docker-ps-list-running-containers)
4. [Network Configuration Commands](#7-docker-network-create-create-a-network)
5. [Volume Management Commands](#10-docker-volume-create-create-a-volume)
6. [Logging and Monitoring Commands](#12-docker-logs-display-container-logs)
7. [Registry and Repository Commands](#14-docker-push-push-an-image-to-a-registry)
8. [Miscellaneous Commands](#16-docker-exec-run-a-command-in-a-running-container)

## Container Lifecycle Management Commands

### 1. docker run: Run a container
- **Usage:** `docker run [options] <image>`
- **Description:** Create and start a container from an image. Options can specify container names, ports, volumes, and more.

```bash
# Run a container interactively with a specific image
docker run -it ubuntu

# Run a detached container with a specified name
docker run -d --name my_container nginx
```

### 2. docker start: Start one or more stopped containers
- **Usage**: `docker start [options] <container>`
- **Description**: Start one or more stopped containers.

```bash
# Start a stopped container
docker start my_container
```

### 3. docker stop: Stop one or more running containers
- **Usage**: `docker stop [options] <container>`
- **Description**: Stop one or more running containers.

```bash
# Stop a running container
docker stop my_container
```

### 4. docker restart: Restart a container
- **Usage**: `docker restart [options] <container>`
- **Description**: Restart a running, paused, or stopped container.

```bash
# Restart a container
docker restart my_container
```

### 5. docker pause: Pause all processes within one or more containers
- **Usage**: `docker pause <container>`
- **Description**: Pause all processes within one or more containers.

```bash
# Pause a running container
docker pause my_container
```

### 6. docker unpause: Unpause all processes within one or more containers
- **Usage**: `docker unpause <container>`
- **Description**: Unpause all processes within one or more containers.

```bash
# Unpause a paused container
docker unpause my_container
```

### 7. docker rm: Remove one or more containers
- **Usage**: `docker rm [options] <container>`
- **Description**: Remove one or more containers.

```bash
# Remove a stopped container
docker rm my_container
```

### 8. docker kill: Kill one or more running containers
- **Usage**: `docker kill [options] <container>`
- **Description**: Kill one or more running containers.

```bash
# Kill a running container
docker kill my_container
```

### 9. docker exec: Run a command in a running container
- **Usage**: `docker exec [options] <container> <command>`
- **Description**: Run a command in a running container.

```bash
# Execute a command in a running container
docker exec my_container ls /app
```

## Image Management Commands
### 10. docker build: Build an image
- **Usage**: `docker build [options] <path|url>`
- **Description**: Build an image from a Dockerfile.
```bash
# Build an image from the current directory
docker build -t my_image:latest .
```
### 11. docker pull: Pull an image or a repository from a registry
- **Usage**: `docker pull [options] <name[:tag]|@digest>`
- **Description**: Pull an image or a repository from a registry.
```bash
# Pull a specific image from Docker Hub
docker pull ubuntu:latest
```

### 12. docker push: Push an image to a registry
- **Usage**: `docker push [options] <name[:tag]>`
- **Description**: Push an image to a registry.
```bash
# Push an image to Docker Hub
docker push my_image:latest
```

### 13. docker images: List images
- **Usage**: `docker images [options] [repository[:tag]]`
- **Description**: List images.
```bash
# List all images
docker images
```

### 14. docker rmi: Remove one or more images
- **Usage**: `docker rmi [options] <image>`
- **Description**: Remove one or more images.

```bash
# Remove an image
docker rmi my_image:latest
```

### 15. docker tag: Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
- **Usage**: `docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]`
- **Description**: Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE.
```bash
# Tag an image with a new name and optional tag
docker tag my_image:latest my_repo/my_image:v1.0
```

## List and Inspection Commands

### 16. docker ps: List running containers
- **Usage**: `docker ps [options]`
- **Description**: List running containers.

```bash
# List all running containers
docker ps
```

### 17. docker ps -a: List all containers (including stopped ones)
- **Usage**: `docker ps -a [options]`
- **Description**: List all containers (including stopped ones).
```bash
# List all containers
docker ps -a
```

### 18. docker inspect: Display detailed information on one or more containers/images
- **Usage**: `docker inspect [options] <name|id>`
- **Description**: Display detailed information on one or more containers/images.

```bash
# Inspect a container
docker inspect my_container
```

### 19. docker logs: Display container logs
- **Usage**: `docker logs [options] <container>`
- **Description**: Display the logs of a container.
```bash
# Display the logs of a container
docker logs my_container
```

### 20. docker events: Get real-time events from the server
- **Usage**: `docker events [options]`
- **Description**: Get real-time events from the server.

```bash
# Get real-time events
docker events
```
## Network Configuration Commands
### 21. docker network create: Create a network
- **Usage**: `docker network create [options] <network>`
- **Description**: Create a network.

```bash
# Create a bridge network
docker network create my_network
```

### 22. docker network ls: List networks
- **Usage**: `docker network ls [options]`
- **Description**: List networks.

```bash
# List all networks
docker network ls
```

### 23. docker network inspect: Display detailed information on one or more networks
- **Usage**: `docker network inspect [options] <network>`
- **Description**: Display detailed information on one or more networks.
```bash
# Inspect a network
docker network inspect my_network
```

### 24. docker network connect: Connect a container to a network
- **Usage**: `docker network connect [options] <network> <container>`
- **Description**: Connect a container to a network.
```bash
# Connect a container to a network
docker network connect my_network my_container
```

### 25. docker network disconnect: Disconnect a container from a network
- **Usage**: `docker network disconnect [options] <network> <container>`
- **Description**: Disconnect a container from a network.

```bash
# Disconnect a container from a network
docker network disconnect my_network my_container
```

## Volume Management Commands
### 26. docker volume create: Create a volume
- **Usage**: `docker volume create [options] <volume>`
- **Description**: Create a volume.

```bash
# Create a volume
docker volume create my_volume
```
### 27. docker volume ls: List volumes
- **Usage**: `docker volume ls [options]`
- **Description**: List volumes.
```bash
# List all volumes
docker volume ls
```

### 28. docker volume inspect: Display detailed information on one or more volumes
- **Usage**: `docker volume inspect [options] <volume>`
- **Description**: Display detailed information on one or more volumes.

```bash
# Inspect a volume
docker volume inspect my_volume
```

### 29. docker volume rm: Remove one or more volumes
- **Usage**: `docker volume rm [options] <volume>`
- **Description**: Remove one or more volumes.

```bash
# Remove a volume
docker volume rm my_volume
```

## Logging and Monitoring Commands
### 30. docker logs: Display container logs
- **Usage**: `docker logs [options] <container>`
- **Description**: Display the logs of a container
```bash
# Display the logs of a container
docker logs my_container
```
### 31. docker stats: Display a live stream of container(s) resource - Usage statistics
- **Usage**: `docker stats [options] <container>`
- **Description**: Display a live stream of container(s) resource - Usage statistics.
```bash
# Display live resource - Usage statistics of a container
docker stats my_container
```
## Registry and Repository Commands

### 32. docker login: Log in to a Docker registry
- **Usage**: `docker login [options] [server]`
- **Description**: Log in to a Docker registry.

```bash
# Log in to Docker Hub
docker login
```

### 33. docker logout: Log out from a Docker registry
- **Usage**: `docker logout [server]`
- **Description**: Log out from a Docker registry.

```bash
# Log out from Docker Hub
docker logout
```

### 34. docker search: Search for an image on Docker Hub
- **Usage**: `docker search [options] <image>`
- **Description**: Search for an image on Docker Hub.
```bash
# Search for an image on Docker Hub
docker search ubuntu
```

### 35. docker push: Push an image to a registry
- **Usage**: `docker push [options] <name[:tag]>`
- **Description**: Push an image to a registry.
```bash
# Push an image to Docker Hub
docker push my_image:latest
```
### 36. docker pull: Pull an image or a repository from a registry
- **Usage**: `docker pull [options] <name[:tag]|@digest>`
- **Description**: Pull an image or a repository from a registry.

```bash
# Pull a specific image from Docker Hub
docker pull ubuntu:latest
```

## Miscellaneous Commands
### 37. docker exec: Run a command in a running container
- **Usage**: `docker exec [options] <container> <command>`
- **Description**: Run a command in a running container.

```bash
# Execute a command in a running container
docker exec my_container ls /app
```

### 38. docker cp: Copy files/folders between a container and the local filesystem
- **Usage**: `docker cp [options] <container>:<source_path> <destination_path>`
- **Description**: Copy files/folders between a container and the local filesystem.
```bash
# Copy a file from a container to the local filesystem
docker cp my_container:/app/file.txt /local/path
```

### 39. docker build: Build an image from a Dockerfile
- **Usage**: `docker build [options] <path|url>`
- **Description**: Build an image from a Dockerfile.
```bash
# Build an image from the current directory
docker build -t my_image:latest .
```

### 40. docker version: Show the Docker version information
- **Usage**: `docker version [options]`
- **Description**: Show the Docker version information.
```bash
# Show Docker version information
docker version
```

### 41. docker info: Display system-wide information
- **Usage**: `docker info [options]`
- **Description**: Display system-wide information.

```bash
# Display system-wide information
docker info
```

## Acknowledgements
Useful YouTube links:
- [How to create a great dev environment with Docker](https://www.youtube.com/watch?v=0H2miBK_gAk&t=918s)

- [Docker Tutorial for Beginners - A Full DevOps Course on How to Run Applications in Containers](https://www.youtube.com/watch?v=fqMOX6JJhGo)


## Author / Contributor
These snippets were gathered and organized by **Vladimir Balabanov** / username: __Grrr1337__.

