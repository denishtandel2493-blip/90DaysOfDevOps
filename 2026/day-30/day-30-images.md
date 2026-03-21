# Day-30 Challenge

## Docker Images
    A Docker Image is like a blueprint or template used to create containers
            Image = Class (template)
            Container = Object (running instance)
    A Docker Image is a read-only file that contains:
            Application code
            Runtime (Node.js, Python, etc.)
            Libraries & dependencies
            Environment variables
            Configuration files
    Alpine is smaller because it uses musl + BusyBox + minimal packages, while Ubuntu uses glibc + full GNU tools + more dependencies
<img width="1029" height="887" alt="image" src="https://github.com/user-attachments/assets/c7d0080d-5772-47bf-abd8-c928d9181350" />

##  Image Layers
    A Docker Image is built using multiple layers stacked on top of each other.
    Each instruction in a Dockerfile creates one layer 
    A layer is a read-only snapshot Represents a change (install, copy, config) Cached and reusable
<img width="1157" height="473" alt="image" src="https://github.com/user-attachments/assets/bddea98a-b109-43cc-8947-3d1ad0d2e563" />

## Container Lifecycle

    A container lifecycle describes the different states a container goes through from creation to deletion
    A container moves through states like created, running, stopped, and removed, and Docker manages transitions using commands like run, start, stop, and rm
<img width="1155" height="448" alt="image" src="https://github.com/user-attachments/assets/790c46c3-2ef1-420f-932b-d89d9fbfa844" />
<img width="1167" height="641" alt="image" src="https://github.com/user-attachments/assets/9cca5c1f-d423-484a-a7b1-b6238d5d46b4" />

##  Working with Running Containers
    Once a container is running, you don’t rebuild it—you interact with it
    To work with running containers, we use commands like docker exec, logs, inspect, and stats for debugging, monitoring, and interaction
    Detached mode means the container runs in the background (you get your terminal back immediately)
