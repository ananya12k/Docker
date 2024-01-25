# Docker

In this we will learn about docker and how to use it.

# Before Docker

For a beginner, where are these enterprise apps running?

In various environments like:

- Servers
- Virtual Machines
- Data Centers
- Cloud

What used to happen before docker?

- We used to have a server
- Only one app could run on one server
- If we wanted to run multiple apps, we needed multiple servers, load increases.
- So for a new app, we needed a new server, which was expensive.

This in turn becomes liablity for the company since we need moere hardware, more maintenance, more cost.

Now the question is who solves this problem?

- <b>VMWare</b> - how?
  By using virtualization, we can run multiple virtual machines on a single server.(Virtual Machines are like a computer inside a computer)

This was nice but it had some problems:

- It needed its own OS. For example, if we have 3 VMs, we need 3 OSs.

Modern Problems(Not working in my machine):

- Version conflicts
- Dependency conflicts
- Environment conflicts
- Migration of apps from one machine to another
- Open source software not working on all machines
- Not able to run apps on different OSs

Solution for VM:

- Companies started run apps in isolation (New VM for each app)
- Containers were born
- Containers are like VMs but they don't need their own OS
- They share the OS of the host machine
- They are lightweight
- They are fast
- They are portable
- They are open source

# What is a container?

Container are VM like machines but they don't need their own OS. They share the OS of the host machine. They are lightweight, fast, portable and open source.

Imagine a container as a box. This box has everything that an app needs to run. It has the code, it has the runtime, it has the system tools, it has the libraries, it has the OS. Everything that an app needs to run is inside this box. So the app can run on any machine that has docker installed on it.

# What is Docker?

Docker is a containerization platform. It is a platform to build, run and ship applications in containers.Help us to run apps in isolation.

All the docker containers are based on lightweight linux distributions.

# Docker Architecture

Docker has runtime, docker engine, orchestration, docker registry, docker client, docker hub.

## Docker Runtime

Dockers runtime is the container engine. It is the core of docker. It is the part that runs the containers. It is the part that runs the apps in isolation. It is the part that runs the apps in the containers. It is the part that runs the apps in the boxes.

### Low level components of docker runtime

- runc
- containerd
- libcontainer

## Docker Engine

- docker engine
- docker daemon
- docker client

## Docker Orchestration

Docker orchestration is the part that helps us to manage multiple containers. It helps us to manage multiple containers in multiple machines. It helps us to manage multiple containers in multiple machines in multiple environments. It helps us to manage multiple containers in multiple machines in multiple environments in multiple clouds.

- Docker Swarm
- Kubernetes

## Docker Registry

Docker registry is the part that helps us to store docker images. It is the part that helps us to store the boxes. It is the part that helps us to store the containers. It is the part that helps us to store the apps. It is the part that helps us to store the apps in the containers. It is the part that helps us to store the apps in the boxes.

- Docker Hub
- Docker Registry

## Docker Client

Docker client is the part that helps us to interact with docker. It is the part that helps us to interact with the docker engine. It is the part that helps us to interact with the docker runtime. It is the part that helps us to interact with the docker orchestration. It is the part that helps us to interact with the docker registry. It is the part that helps us to interact with the docker hub. It is the part that helps us to interact with the docker registry.

## Docker Hub

Docker hub is the part that helps us to store docker images. It is the part that helps us to store the boxes. It is the part that helps us to store the containers. It is the part that helps us to store the apps. It is the part that helps us to store the apps in the containers. It is the part that helps us to store the apps in the boxes.

# Docker Installation

- Go to https://docs.docker.com/get-docker/
- Click on the appropriate OS
- Follow the instructions

# Images and Containers

## Images

Images are actual artifacts that contain actual code, runtime, system tools, libraries, OS. They contain all the configurations that are needed to run an app.
Images are based on lightweight linux distributions.
The images have OS file, dependencies, libraries, code, runtime, system tools, configurations, environment variables, entrypoint, command, metadata, etc.

## Containers

Containers are the running instances of the images.

# Docker Commands

- `docker version` - To check the version of docker
- `docker info` - To check the info of docker
- `docker` - To check all the commands of docker
- `docker run hello-world` - To run a container
- `docker ps` - To check the running containers
- `docker ps -a` - To check all the containers
- `docker images` - To check all the images
- `docker pull <image_name>` - To pull an image from docker hub
- `docker rmi <image_name>` - To remove an image
- `docker rm <container_name>` - To remove a container
- `docker run -it <image_name>` - To run a container in interactive mode
- `docker run -it <image_name> bash` - To run a container in interactive mode with bash
- `docker run -it <image_name> sh` - To run a container in interactive mode with sh
- `docker run -it <image_name> zsh` - To run a container in interactive mode with zsh
- `docker run -it <image_name> /bin/bash` - To run a container in interactive mode with bash
- `docker run -it <image_name> /bin/sh` - To run a container in interactive mode with sh
- `docker run -it <image_name> /bin/zsh` - To run a container in interactive mode with zsh
- `docker start <container_name>` - To start a container
- `docker stop <container_name>` - To stop a container
- `docker exec -it <container_name> bash` - To run a container in interactive mode with bash
- `docker exec -it <container_name> sh` - To run a container in interactive mode with sh
- `docker run -p <host_port>:<container_port> <image_name>` - To run a container with port mapping
- `docker logs <container_name>` - To check the logs of a container
- `docker logs -f <container_name>` - To check the logs of a container in real time
- `docker run -d <image_name>` - To run a container in detached mode
- `docker run -d -p <host_port>:<container_port> <image_name>` - To run a container in detached mode with port mapping
- `docker run -d -p <host_port>:<container_port> --name <container_name> <image_name>` - To run a container in detached mode with port mapping and name
- `docker run -d -p <host_port>:<container_port> --name <container_name> --env <env_variable_name>=<env_variable_value> <image_name>` - To run a container in detached mode with port mapping, name and environment variable
- `docker run -d -p <host_port>:<container_port> --name <container_name> --env <env_variable_name>=<env_variable_value> --env <env_variable_name>=<env_variable_value> <image_name>` - To run a container in detached mode with port mapping, name and multiple environment variables
- `docker network ls` - To check the networks
- `docker network create <network_name>` - To create a network
- `docker network inspect <network_name>` - To inspect a network
- `docker inspect <container_name>` - To inspect a container
- `docker images` - To check all the images
- `docker build -t <image_name> .` - To build an image
- `docker build -t <image_name> <path_to_dockerfile>` - To build an image
- `docker build -t <image_name>:<tag_name> .` - To build an image with tag
- `docker build -t <image_name>:<tag_name> <path_to_dockerfile>` - To build an image with tag
- `docker build -t <dockerhub_username>/<image_name>:<tag_name> .` - To build an image with tag
- `docker build -t <dockerhub_username>/<image_name>:<tag_name> <path_to_dockerfile>` - To build an image with tag
- `docker push <dockerhub_username>/<image_name>:<tag_name>` - To push an image to docker hub
- `docker pull <dockerhub_username>/<image_name>:<tag_name>` - To pull an image from docker hub
- `docker login` - To login to docker hub
- `docker tag <image_name>:<tag_name> <dockerhub_username>/<image_name>:<tag_name>` - To tag an image
- `docker volume ls` - To check the volumes
- `docker volume create <volume_name>` - To create a volume
- `docker volume inspect <volume_name>` - To inspect a volume
- `docker volume rm <volume_name>` - To remove a volume
- `docker volume prune` - To remove all the volumes

# Dockerfile

Dockerfile is a file that contains all the instructions that are needed to build an image.

# Dockerfile Instructions

- `FROM` - To specify the base image
- `RUN` - To run a command
- `CMD` - To run a command when the container is started
- `EXPOSE` - To expose a port
- `ENV` - To set an environment variable
- `WORKDIR` - To set the working directory
- `COPY` - To copy files from host to container
- `ADD` - To copy files from host to container
- `ENTRYPOINT` - To run a command when the container is started
- `VOLUME` - To create a volume
- `USER` - To set the user
- `ARG` - To set the arguments
- `ONBUILD` - To run a command when the image is used as a base image

# Dockerfile Instructions Examples

- `FROM <base_image>` - To specify the base image
- `RUN <command>` - To run a command
- `CMD <command>` - To run a command when the container is started
- `EXPOSE <port>` - To expose a port
- `ENV <env_variable_name> <env_variable_value>` - To set an environment variable
- `WORKDIR <path>` - To set the working directory
- `COPY <source> <destination>` - To copy files from host to container
- `ADD <source> <destination>` - To copy files from host to container
- `ENTRYPOINT <command>` - To run a command when the container is started
- `VOLUME <path>` - To create a volume
- `USER <user>` - To set the user
- `ARG <arg_name> <arg_value>` - To set the arguments
- `ONBUILD <command>` - To run a command when the image is used as a base image
