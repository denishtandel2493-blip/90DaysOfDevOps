# Day-31 Challenge
## First Dockerfile
    A Dockerfile is a text file that tells Docker how to build an image for your application
<img width="816" height="267" alt="image" src="https://github.com/user-attachments/assets/bea59259-3efb-41e2-804a-0cd307726e3a" />
<img width="973" height="1000" alt="image" src="https://github.com/user-attachments/assets/3a1efb4f-d31d-49bb-a68d-c4bb707f4da1" />
<img width="966" height="982" alt="image" src="https://github.com/user-attachments/assets/8c59e079-f787-4d0c-aca6-be3b4d5c7c14" />

## Dockerfile Instructions
    Dockerfile that uses all the instructions with Docker
    Instruction	Purpose
        FROM - Base image
        RUN  - Execute commands during build
        COPY - Copy files from host
        ADD	 - Copy + extract files
        WORKDIR	-  Set working directory
        EXPOSE	-  Inform container port
        CMD	-      Default command
        ENTRYPOINT	-  Main executable

<img width="1023" height="522" alt="image" src="https://github.com/user-attachments/assets/053b77b9-5806-44c2-98ba-705d207c3005" />
<img width="1018" height="991" alt="image" src="https://github.com/user-attachments/assets/9188bcfa-0ff6-4aee-8d59-be5b691c1003" />
<img width="1009" height="980" alt="image" src="https://github.com/user-attachments/assets/92d3f11c-a168-45b5-90a0-3766c65e0c76" />

## CMD vs ENTRYPOINT
### CMD
        CMD was Replace by the new command.
        Default command for the container that can be overridden when running the container.
<img width="1016" height="548" alt="image" src="https://github.com/user-attachments/assets/f29b3257-4f4a-48ca-94cd-dfc069af948d" />

### ENTRYPOINT
        Defines the main executable of the container, and arguments from docker run are appended to it.
