# Day-29 Challenge
# Docker
    Docker is a containerization platform that allows you to package an application and its dependencies into a container so it runs everywhere —- on your laptop, server, or cloud.
# Containers
    Containers run on top of the host OS kernel.
# Virtual Machine (VM)
    A VM runs on top of a Hypervisor and includes a full operating system.
    A container shares the host OS kernel (lightweight & fast), while a virtual machine runs its own full OS (heavier but more isolated).
# Docker architecture
    Docker architecture is a client-server model where the Docker client communicates with the Docker daemon, which manages containers using images stored locally or in a registry.
<img width="325" height="165" alt="image" src="https://github.com/user-attachments/assets/6ecd01d2-0e23-4566-b2f2-a24ea77fe4cf" />

# Install Docker
<img width="1313" height="965" alt="image" src="https://github.com/user-attachments/assets/d611ab44-9597-4601-bacc-71e44130bdd5" />
<img width="1288" height="1014" alt="image" src="https://github.com/user-attachments/assets/81546555-c2a9-419b-9f66-6bfa425855d2" />

# Run the hello-world container
    Hello from Docker!
    This message shows that your installation appears to be working correctly.
    To generate this message, Docker took the following steps:
     1. The Docker client contacted the Docker daemon.
     2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
     3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
     4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.
<img width="761" height="709" alt="image" src="https://github.com/user-attachments/assets/fbc102ef-4ca9-40ab-b2c8-c68a78559e64" />

# Run Real Containers
    -- Docker pulled the Nginx image
    -- Created a container Exposed container port 80 
    -- Mapped it to your machine’s port 80
    -- Nginx inside container started serving web pages
<img width="1354" height="460" alt="image" src="https://github.com/user-attachments/assets/76845917-4ad1-4b72-b504-1ee264808f0f" />
