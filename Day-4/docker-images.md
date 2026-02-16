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
docker images

2) Pull image from DockerHub
docker pull nginx

3) Build image using Dockerfile
docker build -t myapp:1.0 .

4) Remove an image
docker rmi nginx

5) Remove all unused images
docker image prune -a

6) Inspect image details
docker inspect nginx

7) Tag an image
docker tag myapp:1.0 myrepo/myapp:1.0

8) Push image to DockerHub
docker push myrepo/myapp:1.0

✅ Docker Container Commands:
==============================

1) Run a container
docker run nginx

2) Run container in background (detached mode)
docker run -d nginx

3) Run container with name
docker run -d --name web nginx

4) Check running containers
docker ps

5) Check all containers (running + stopped)
docker ps -a

6) Stop a container
docker stop web

7) Start a stopped container
docker start web

8) Restart a container
docker restart web

9) Remove a container
docker rm web

10) Remove container forcefully
docker rm -f web

11) View container logs
docker logs web

12) Login inside container
docker exec -it web bash

13) Check container details
docker inspect web