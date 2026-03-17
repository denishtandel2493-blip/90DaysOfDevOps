# Day-50 Challenge
## Recall the Kubernetes Story
    Kubernetes was created to automate deployment, scaling, and management of containerized applications.
    
    Docker runs containers, but Kubernetes solves the problem of managing, scaling, and maintaining containers across multiple systems automatically.
    
    Kubernetes was created by Google and inspired by their internal system Borg, which managed large-scale containerized workloads efficiently.
    
    Kubernetes means “helmsman”, symbolizing how it steers and manages containerized applications.

## Draw the Kubernetes Architecture
<img width="982" height="691" alt="image" src="https://github.com/user-attachments/assets/75f84af7-0173-4c53-943d-f2c19c71dd42" />

### API Serevr
    API Server is the central control point of Kubernetes that handles all requests and maintains the cluster state.
### etcd
    etcd is the distributed database that stores all Kubernetes cluster data and acts as the single source of truth.
### Scheduler
    Scheduler is the component that selects the best node for a Pod to run on based on resources and constraints
### Control Manager
    Controller Manager continuously ensures the cluster’s actual state matches the desired state by running control loops.
### kublet
    Kubelet is the node agent that ensures containers are running as per the instructions from the API Server
### kube-proxy
    kube-proxy is the networking component that routes and load-balances traffic between Services and Pods in Kubernetes.
### Container Runtime
    Container Runtime is the software that pulls images and runs containers on Kubernetes nodes.

##  Install kubectl
<img width="1029" height="589" alt="image" src="https://github.com/user-attachments/assets/814478ee-3cc6-41a4-84af-ee86f4f8a197" />

    
    
