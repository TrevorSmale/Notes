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



