# Podman
A OCI based container engine created by RedHat that is mostly interchangeable with Docker with some key differences

## Podman is slightly different

    * Podman is an alternative to Docker that uses the same command line interface (CLI) and the same container image format.
    * Unlike Docker, Podman does not require a daemon to be running in order to manage and run containers.
    * Podman uses the same container runtime as CRI-O and Buildah, which is runc.
    * Podman supports rootless containers, which means that it can run containers without requiring the user to have root privileges.
    * Podman does not have the daemon attack surface and does not have any daemon-specific configuration options.
    * Podman does not support Swarm mode, which is Docker's built-in container orchestration.
    * Podman can be used with Kubernetes, which is a popular container orchestration platform.
    * Podman support many features like cgroups v1 and v2, namespaces, and SELinux that are not available in Docker.

## Example CLI build command

podman build -t myhugo:latest --build-arg HUGO_VERSION=0.78.2 -f Dockerfile .

## Trouble pulling images from Fedora/Redhat container directories

There is seemingly an issue with pulling container images from the suggested sources. I am working from Fedora 37 and this issue seems to stem from permission issues or build scripts. I will be looking into this at a later date.

## Able to build from Docker.io

So I have successfully pulled down/built containers with vertualized open ports from the Docker.io hub. This works similarly to my past Docker experiences.
I can use the $PS command to see built and running containers. furthermore, I can stop and remove the running contianers with the same CLI commands as well.