# Day-58 Challenge
## Metrics Server and Horizontal Pod Autoscaler (HPA)
    These two components work together in Kubernetes to automatically scale your application based on load
### Metrics Server
        The Metrics Server is a lightweight Kubernetes add-on that: Collects resource usage data like: CPU usage, Memory usage 
        It gathers this data from:  Kubelets running on each node, And makes it available to:  kubectl top, HPA (Horizontal Pod Autoscaler)          
### Horizontal Pod Autoscaler (HPA)
        The Horizontal Pod Autoscaler automatically: Increases Pods when load is high, Decreases Pods when load is low
        How HPA Works :- Metrics Server provides CPU/memory data, HPA checks usage vs target, HPA adjusts number of Pods
## Install the Metrics Server
        For local clusters (like kind/minikube), you may need:
           # kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml 
<img width="789" height="505" alt="image" src="https://github.com/user-attachments/assets/d93210ed-315a-4cee-a52a-cee6cb308cee" />

## Explore kubectl top
    The kubectl top command lets you quickly view CPU and memory usage of your cluster — powered by the Metrics Server
    A built-in command to check live resource usage:  Nodes (entire machines), Pods (individual workloads)     
    It is similar to: top command in Linux,  Task Manager in Windows
<img width="788" height="746" alt="image" src="https://github.com/user-attachments/assets/ccc61ec5-fe62-4f6e-a0ef-d35dcd720a50" />

## Create a Deployment with CPU Requests
    To make features like autoscaling work properly, you must define CPU requests in your Pod spec. This tells Kubernetes:
    Reserve this much CPU for my container, Required for Horizontal Pod Autoscaler, Helps scheduler place Pods correctly
    Enables accurate metrics from Metrics Server
<img width="802" height="696" alt="image" src="https://github.com/user-attachments/assets/4d9f5f3b-73d6-4c7d-a2b8-b84b81228bce" />

## Create an HPA (Imperative)
    create a Horizontal Pod Autoscaler using a single kubectl command (no YAML needed)
<img width="1301" height="510" alt="image" src="https://github.com/user-attachments/assets/05ac3599-7f8b-4414-995c-2e48e2018b97" />

## Generate Load and Watch Autoscaling
    Load hits php-apache, CPU usage rises above 50% target, Horizontal Pod Autoscaler increases replicas step by step
    Eventually CPU stabilizes near target
    HPA usually scales to ~3–7 replicas under moderate load
<img width="721" height="660" alt="image" src="https://github.com/user-attachments/assets/31075c01-7c15-4a4e-b7f6-554addf3f885" />

## Create an HPA from YAML (Declarative)
    Instead of using an imperative command, you can define the Horizontal Pod Autoscaler in YAML for better version control and reproducibility
    In a Horizontal Pod Autoscaler, the behavior section controls how fast and how aggressively scaling happens 
    “Scaling rules and limits” (not when to scale, but how to scale)
<img width="1219" height="1006" alt="image" src="https://github.com/user-attachments/assets/6c548699-68d3-4801-a046-374a24f272ee" />


       
           
    
    
    
            
                  
           
