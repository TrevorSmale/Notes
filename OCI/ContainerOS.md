# Container Friendly Operating Systems
## Operating systems and/or Distributions that work well in a container based workflow

1. BusyBox (Linux)
   
   BusyBox is a lightweight and versatile Linux distribution that includes a variety of stripped-down Unix tools and utilities. It's designed to be used on embedded devices and other systems with limited resources, such as routers, set-top boxes, and smartphones. BusyBox can function as a complete operating system or as a component of a larger system, depending on the needs of the user. It includes a wide range of commands and can be customized to include only the tools needed for a particular task. BusyBox is open source software and is distributed under the terms of the GNU General Public License. Learn more at the official site: https://www.busybox.net/

2. Alpine (Linux)

    Alpine Linux is a lightweight, security-oriented Linux distribution that is designed to be small and efficient. It features a minimalist design and includes only essential packages, making it a popular choice for servers, containers, and embedded devices. Alpine uses the musl libc library instead of the more common glibc, which contributes to its small size and enhanced security. Alpine also includes a package manager called apk, which is used to manage and install software packages. The distribution is available in both standard and hardened versions, which includes additional security features such as kernel hardening and compiler security flags. Alpine is open source software and is distributed under the terms of the MIT License. Learn more at the official site: https://alpinelinux.org/
   
3. TinyCore (Linux)

    TinyCore Linux is an ultra-minimalist Linux distribution that is designed to be extremely lightweight and fast. It is a fully functional operating system that can be run from RAM, which means that it can be booted from a USB drive or other removable media and run entirely in memory. TinyCore includes only the essential components necessary to run a functional operating system, including the BusyBox utilities and a minimal X Window System desktop environment. Additional software can be installed using the distribution's package manager or by loading extensions into RAM. TinyCore is open source software and is distributed under the terms of the GNU General Public License. Learn more at the official site: https://www.tinycorelinux.net/
   
4. Nix OS (Linux)

    NixOS is a Linux distribution that takes a unique approach to package management and system configuration. It uses a purely functional package manager called Nix, which allows users to install and manage packages without worrying about dependency conflicts or versioning issues. The configuration of the entire system is also declarative and reproducible, meaning that changes to the configuration are tracked and can be easily rolled back if necessary. NixOS includes a wide range of software packages and supports multiple desktop environments and window managers. The distribution is highly customizable and includes a powerful command-line interface for system management. NixOS is open source software and is distributed under the terms of the GNU General Public License. Learn more at the official site: https://nixos.org/
   
5. Flat Container (Linux)

    Flatcar Container Linux is a lightweight, secure, and scalable Linux distribution that is optimized for container workloads. It is designed to be deployed as a container runtime host, providing a minimal and secure environment for running containerized applications. Flatcar Container Linux includes a wide range of container runtimes and orchestrators, such as Docker, Kubernetes, and systemd-nspawn. The distribution is also highly customizable and can be tailored to meet the specific needs of an organization. Flatcar Container Linux is built from the same codebase as CoreOS, a popular container-focused Linux distribution that has been acquired by Red Hat. Flatcar Container Linux is open source software and is distributed under the terms of the Apache License. Learn more at the official site: https://www.flatcar-linux.org/