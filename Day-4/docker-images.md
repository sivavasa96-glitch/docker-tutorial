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
docker login

docker push myrepo/myapp:1.0
```
Run command options
=====================

```hcl
 -rm this used to remove a container once we exit from it
 -it this is used to open the shell or interactive termianl in tha container where we can file linux commands
 --name this is used to give a customised name to our container
 -p This is used for port mapping.The port no on left side of :     is called external port and port no on right of : is called      internal port no(eg -p 3308:3306)
 -v This is used for attaching volumes
  -P This is used to publish the port number of a docker      container
  -e this used to pass environment variables
  -a used to attach stndin and stdout
```

✅ Docker Container Commands:
==============================

1) To see the list of all running containers
```hcl
docker container ls
```
2) Run a container
```hcl
docker run nginx
```
3) Run container in background (detached mode)
```hcl
docker run -d nginx
```
4) Run container with name
```hcl
docker run -d --name web nginx
```
5) Check running containers
```hcl
docker ps
```

6) Check all containers (running + stopped)
```hcl
docker ps -a
```
7) Stop a container
```hcl
docker stop web
```
8) Start a stopped container
```hcl
docker start web
```
9) Restart a container
```hcl
docker restart web
```
10) Remove a container
```hcl
docker rm web
```
11) Remove container forcefully
```hcl
docker rm -f web
```
12) View container logs
```hcl
docker logs web
```
13) Login inside container
```hcl
docker exec -it web bash
```
14) Check container details
```hcl
docker inspect web
```
15) To stop all the running containers
```hcl
docker stop $(docker ps -aq)
```
16) To remove all stopped containers
```hcl
docker rm  $(docker ps -aq)
```
17) To remove all running containers
```
docker rm -f $(docker ps -aq)
```
18) To restart a container after 20 seconds
```hcl
docker restart -t 20 containername/containerid
```