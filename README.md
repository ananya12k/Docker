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

Docker is a containerization platform. It is a platform to build, run and ship applications in containers.

# Docker Architecture

Docker has 3 main components:
- Docker Client
- Docker Host
- Docker Registry

Docker Client is the CLI tool that we use to interact with docker. We use it to build, run and ship containers.

Docker Host is the machine that runs the containers. It has the docker daemon running on it. Docker daemon is a background process that manages the containers.

Docker Registry is a registry of docker images. Docker images are used to create containers. Docker images are like templates for containers. Docker images are created using a Dockerfile. Dockerfile is a text file that contains all the commands a user could call on the command line to assemble an image.

# Docker Installation

- Go to https://docs.docker.com/get-docker/
- Click on the appropriate OS
- Follow the instructions

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
<!-- Set usernname and password -->




