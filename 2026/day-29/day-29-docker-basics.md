# Day-29 Challenge
# Docker
    Docker is a containerization platform that allows you to package an application and its dependencies into a container so it runs everywhere —- on your laptop, server, or cloud.
# Containers
    Containers run on top of the host OS kernel.
# Virtual Machine (VM)
    A VM runs on top of a Hypervisor and includes a full operating system.
# A container shares the host OS kernel (lightweight & fast), while a virtual machine runs its own full OS (heavier but more isolated).
# Docker architecture
    Docker architecture is a client-server model where the Docker client communicates with the Docker daemon, which manages containers using images stored locally or in a registry.
    Docker Client
     ↓
    Docker Daemon (dockerd)
     ↓
    Docker Registry (if image not local)
     ↓
    Container Created & Started
