INSTALL DOCKER:
================

A very detailed instructions to install Docker are provide in the below link

https://docs.docker.com/get-docker/

You can create an Ubuntu EC2 Instance on AWS and run the below commands to install docker.

sudo apt update
sudo apt install docker.io -y

Start Docker and Grant Access:
================================

A very common mistake that many beginners do is, After they install docker using the sudo access, they miss the step to Start the Docker daemon and grant acess to the user they want to use to interact with docker and run docker commands.

Install Docker on Ubuntu / Debian:
===================================

1) Remove old versions (if any):
=================================

sudo apt-get remove docker docker-engine docker.io containerd runc

2) Update packages:
====================

sudo apt update
sudo apt install -y ca-certificates curl gnupg lsb-release

3) Add Docker’s official GPG key:
===================================

sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

4) Add Docker repository:
==============================

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

5) Install Docker Engine:
============================

sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

6) Verify Docker installation:
==============================

sudo docker --version
sudo docker run hello-world

✅ Run Docker Without sudo (Recommended):
==========================================

1) Add your user to docker group:
===============================

sudo usermod -aG docker $USER

2) Apply group changes (log out and log in):
=============================================

newgrp docker

3) Test again:
================
docker run hello-world


✅ Check Docker Service Status:
==================================

sudo systemctl status docker

sudo systemctl enable docker

