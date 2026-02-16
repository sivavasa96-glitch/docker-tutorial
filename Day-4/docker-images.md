Images and Containers
=========================

1. A docker image is a combination of bin and lib which are required for a specific process.

or

“A Docker image is a read-only template or blueprint. It contains application code, dependencies, libraries, and required configurations. We use a Docker image to create containers.”

2. A container is a running instance of an image. Any no of containers can be created from a single  docker image

or 

“A Docker container is a running instance of a Docker image. It is the actual environment where the application runs. Containers are lightweight and they share the host OS kernel.”

Docker Image Commands:
======================

1) Check Docker images
```hcl
docker images
```
2) Pull image from DockerHub
```hcl
docker pull nginx
```
3) Build image using Dockerfile
```hcl
docker build -t myapp:1.0 .
```
4) Remove an image
```hcl
docker rmi nginx
```
5) Remove all unused images
```hcl
docker image prune -a
```
6) Inspect image details
```hcl
docker inspect nginx
```
7) Tag an image
```hcl
docker tag myapp:1.0 myrepo/myapp:1.0
```
8) Push image to DockerHub
```hcl
docker push myrepo/myapp:1.0
```

✅ Docker Container Commands:
==============================

1) Run a container
```hcl
docker run nginx
```
2) Run container in background (detached mode)
```hcl
docker run -d nginx
```
3) Run container with name
```hcl
docker run -d --name web nginx
```
4) Check running containers
```hcl
docker ps
```

5) Check all containers (running + stopped)
```hcl
docker ps -a
```
6) Stop a container
```hcl
docker stop web
```
7) Start a stopped container
```hcl
docker start web
```
8) Restart a container
```hcl
docker restart web
```
9) Remove a container
```hcl
docker rm web
```
10) Remove container forcefully
```hcl
docker rm -f web
```
11) View container logs
```hcl
docker logs web
```
12) Login inside container
```hcl
docker exec -it web bash
```
13) Check container details
```hcl
docker inspect web
```