# Day-33 Challenge
## Docker Compose: Multi-Container Basics
    Docker Compose is a tool that helps you define and run multiple Docker containers using a single configuration file (docker-compose.yml)
    For example, a typical application may have:-  1] A Web Application (Python, Node.js, etc.)
    2] A Database (MySQL, PostgreSQL) 3] A Cache (Redis) 
    Instead of starting each container manually, Docker Compose can start and manage all of them together
## Install & Verify
    Docker Compose is installed and available on my machine. 
    I verified it using the command docker compose version, which returned Docker Compose version v5.0.0-desktop.1. 
    Docker is also running successfully with Docker version 29.1.3
<img width="580" height="153" alt="image" src="https://github.com/user-attachments/assets/1779219c-5817-4ee0-8eb0-4e69cee9289c" />

## Your First Compose File
    I created my first Docker Compose file (docker-compose.yml) to run an Nginx web server container. 
    The file defines a service named web, uses the nginx image, and maps port 8080 on the host to port 80 in the container.
    services:
      web:
        image: nginx
        ports:
          - "9090:80"
    I started the container using docker compose up -d and verified it was running successfully with docker compose ps. 
    Accessing http://localhost:8080 displayed the Nginx welcome page.
<img width="1404" height="401" alt="image" src="https://github.com/user-attachments/assets/c6e25b5a-3bbd-4492-8534-a4684b58df20" />

## Two-Container Setup
        


