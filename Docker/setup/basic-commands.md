# Docker Commands


## Docker Basics
- `docker --version` - Check Docker version
- `docker pull [image-name]` - Pull an image from Docker Hub
  - Example: `docker pull nginx`

- `docker images` - List Docker images
- `docker run [options] [image-name]` - Run a container
  - Example: `docker run -d -p 80:80 nginx`

- `docker ps` - List running containers
- `docker ps -a` - List all containers (including stopped ones)
- `docker create busybox echo <hey there>` - Creating a container with echo message
- `docker start <container id> -a` - `-a` to get output
- `docker stop [container-id]` - Stop a container
- `docker kill <container-id>` - Kills a container
- `docker logs <container-id>` - print all the commands 
- `docker start [container-id]` - Start a stopped container
- `docker rm [container-id]` - Remove a container
- `docker rmi [image-id]` - Remove an image

- `docker exec -it <container-id> <docker container for example: (redis-cli)>` - Allows us if we started redis server with `docker run redis server`, this execute command allows us to run multiple containers in different terminals.

## Docker Volumes
- `docker volume create [volume-name]` - Create a volume
- `docker volume ls` - List volumes
- `docker volume inspect [volume-name]` - Inspect a volume
- `docker volume rm [volume-name]` - Remove a volume

## Docker Networks
- `docker network create [network-name]` - Create a network
- `docker network ls` - List networks
- `docker network inspect [network-name]` - Inspect a network
- `docker network rm [network-name]` - Remove a network

## Docker Images
- `docker build -t [image-name] [path-to-dockerfile]` - Build an image from a Dockerfile
- `docker tag [source-image] [target-image]` - Tag an image
- `docker push [image-name]` - Push an image to Docker Hub

## Docker Compose
- `sudo curl -L "https://github.com/docker/compose/releases/download/[version]/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose` - Install Docker Compose on Linux
- `sudo chmod +x /usr/local/bin/docker-compose` - Make Docker Compose executable on Linux
- Docker Desktop includes Docker Compose - Install Docker Compose on macOS and Windows
- `docker-compose up` - Run Docker Compose
- `docker-compose down` - Stop Docker Compose
