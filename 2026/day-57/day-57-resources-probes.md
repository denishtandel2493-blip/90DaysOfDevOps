# Day-57 Challenge
## Resource Requests & Limits
    Resource Requests and Limits define how much CPU and memory a container needs and the maximum it is allowed to use
    Request ----  Minimum resources guaranteed to the container
    Limit  -----  Maximum resources the container can use
    Requests define guaranteed resources for scheduling, while limits define the maximum resources a container can use
    QoS Class = Burstable
<img width="1265" height="943" alt="image" src="https://github.com/user-attachments/assets/cbb788ec-1e95-4eeb-90df-435802e7b3c3" />
<img width="1062" height="729" alt="image" src="https://github.com/user-attachments/assets/ebc96150-6cb9-4604-8dcd-f5569cf615e6" />

## OOMKilled — Exceeding Memory Limits
    OOMKilled (Out Of Memory Killed) happens when a container uses more memory than its defined limit, and Kubernetes terminates it
    OOMKilled occurs when a container exceeds its memory limit, causing the kernel to terminate it immediatel
    An OOMKilled container exits with code 137, which indicates it was terminated by SIGKILL due to exceeding memory limits
<img width="1520" height="988" alt="image" src="https://github.com/user-attachments/assets/87d33870-53ca-419c-b40f-e2890616fe4a" />
<img width="1562" height="675" alt="image" src="https://github.com/user-attachments/assets/5ede3d36-9937-4906-aada-ed2db4adc73e" />

##  Pending Pod — Requesting Too Much
    A Pod is in Pending state when Kubernetes cannot find a node with enough resources to run it
    A Pod remains Pending if the scheduler cannot find a node with sufficient resources to satisfy its requests
    A Pod stays Pending when its resource requests exceed what any node can provide
<img width="769" height="965" alt="image" src="https://github.com/user-attachments/assets/fe4e7c2a-dd43-4f06-bcfd-c3e5a2fcf212" />

## Liveness Probe
    This is how Kubernetes detects and fixes broken containers automatically
    A Liveness Probe checks if a container is still running correctly. If it fails, Kubernetes restarts the container.
    A liveness probe checks container health and restarts it if it becomes unresponsive
    The container restarts repeatedly — you will see the RESTARTS count increasing (1, 2, 3...).
    After the liveness probe fails 3 consecutive times, Kubernetes restarts the container, and the restart count keeps increasing
<img width="936" height="1006" alt="image" src="https://github.com/user-attachments/assets/c9681342-ad23-4c5c-9f66-74865d6ffe26" />

## Readiness Probe
    A Readiness Probe checks if a container is ready to serve requests. If it fails, the Pod is removed from the Service (but NOT restarted).
    NO — the container was NOT restarted
    Why?
    Readiness probe failure:
       Removes Pod from Service traffic
       Does NOT restart container
    Liveness probe failure:
      Restarts container
<img width="1436" height="990" alt="image" src="https://github.com/user-attachments/assets/dbb154e1-c6ab-409b-935b-c27e089d3ad4" />
<img width="1593" height="972" alt="image" src="https://github.com/user-attachments/assets/1a02d140-23bf-465c-9cd1-81b218991a73" />

## Startup Probe
    A Startup Probe is used to handle slow-starting containers. It tells Kubernetes
    Don’t run liveness/readiness checks until the app has fully started
    Without it: 
        Kubernetes may think your app is dead
        Liveness probe might restart it too early  
    With it:
        Startup probe gets time to succeed
        Only then liveness/readiness begin
  















