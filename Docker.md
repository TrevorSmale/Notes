# Docker
## Course notes taken while following the Docker Mastery course by Bret Fisher

## What is Docker?
### Docker is container engine

## The 3 Major functions of Docker

* The docker image - Build
* The docker registry - Ship
* The docker container - Run

## Containers and the Cloud

* The cloud native computing foundation is based around a containerized workflow.
* The container image is kind of like a universal package manager.
* Dockerfile/Container image Anatomy - OCI standard for container images.
* The OCI ‘Open Container Initiative’ 

## Anatomical/Layers of the docker file called ‘stanzas’ are written in JSON
### All of these stanzas together are called a docker image.

* FROM python
* RUN pip install flask
* WORKDIR /app
* COPY ..
* CMD python app.py

## Docker Registries

* The Docker image registry is for the app distribution 
* Each image has a unique SHA hash that represents the unique data within

## Running a Docker image

When an image is run using docker run, the Docker engine will prioritize and place it within a container with its own namespace and IP address. It essentially runs like its own system.

## Container Networking

Containers name space are air gapped from one another by default. So additional commands must be used in order to specify/setup open ports.

## Practice Space

Labs.play-with-docker.com

## Simple Commands

### PS

Processes running

### Docker pull 

will pull a docker image and dependancies using the docker engine. The engine is able to pull images from many different places

## Concepts from Linux

### NAMESPACES

### Control Groups

### UNION MOUNTS

## Why Docker and Containers?

* Isolation
* Environments
* Speed

## Technological progress of development infrastructure

* 90’s saw the exit from mainframes
* 00’’s Saw a change from bare metal to virtual
* 10’s Saw Datacenter to Cloud
* Now Host to Container (Serverless)

## Advantages of containerization

* Develop, Build, Test and Deploy Faster.
* Weekly live Q&A sessions on YouTube 

## Bret Fisher Youtube [https://www.youtube.com/@BretFisher]

## Creating and using containers

Checking the version of Docker and associated infrastructure:

CLI: Docker Version, always used first to verify the status and version

CLI: Docker Info, displays most configuration values of the current docker install

Check all available commands:

CLI: Docker

There is now a hierarchy of commands

This means there are now management and common commands

## Difference between an image and Container

* An image is the application we want to run
* A container is an instance of that image running as a process
* You can have many containers running off the same image
* In this lecture our image will be the Nginx web server
* Dockers default image "registry" is called Docker Hub (hub.docker.com)

## Running an Nginx container

CLI: docker container run --publish 80:80 nginx

* Downloaded image 'nginx' from Docker Hub
* Started a new container from that image
* Opened port 80 on the host IP
* Routes that traffic to the container IP, port 80

Note: you will get a "bind" error if the left number [Host port] is already in use. If this is the case, an easy alternative is 8888

## Viewing container status in the CLI

docker container ls - will show regular status

docker container ls -a - will show additional info

## Stopping a running container

Docker stop + first 3 - 4 characters of unique id

## Naming a container

docker container run --publish 80:80 --detach --name webhost nginx