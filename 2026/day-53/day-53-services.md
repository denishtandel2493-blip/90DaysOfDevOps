# Day-53 Challenge
## Kubernetes Services
    In Kubernetes, a Service is used to expose your application (Pods) and make them accessible—either inside the cluster or outside
    A Service is like a stable entry point (fixed IP + DNS name) for a group of Pods.
    Problem:
        Pods are dynamic (they get deleted/recreated)
        Their IPs keep changing
    Solution:
        Service provides a fixed IP and name to access Pods reliably

## Deploy the Application
    First, create a Deployment that you will expose with Services. Create app-deployment.yaml
<img width="1207" height="686" alt="image" src="https://github.com/user-attachments/assets/10442190-502f-4eae-b92b-302785190c79" />

## ClusterIP Service (Internal Access)
    In Kubernetes, a ClusterIP Service is the default type of Service used for communication inside the cluster only
    A ClusterIP Service:
          Gets a private IP
          Is accessible only within the cluster
          Cannot be accessed from outside (Browser, Internet)
          It acts as an internal load balancer
    ClusterIP Service provides internal load balancing and stable DNS to access dynamic Pods
<img width="872" height="479" alt="image" src="https://github.com/user-attachments/assets/f1a370bf-ae8a-48d3-8a5a-288abc8f8bbf" />
<img width="874" height="516" alt="image" src="https://github.com/user-attachments/assets/2403f5b8-5988-457c-8aa0-d980f96e914b" />

## Discover Services with DNS
    In Kubernetes, every Service automatically gets a DNS name, so Pods don’t need to remember IP addresses
    Kubernetes has a built-in DNS server. Every Service gets a DNS entry automatically
    nslookup on a Kubernetes Service returns the ClusterIP, which matches the CLUSTER-IP field from kubectl get services
<img width="793" height="961" alt="image" src="https://github.com/user-attachments/assets/2773325b-94e5-4363-bff2-6c6622f746de" />

## NodePort Service (External Access via Node)
    In Kubernetes, a NodePort Service is used to expose your application outside the cluster using a port on each node.
    A NodePort Service:
          Opens a port on every node (worker machine)
          Allows access from outside the cluster  
          Forwards traffic to the Service → then to Pods
    NodePort exposes services on node IPs, but in container-based clusters like kind, additional port mapping is required to access them from the host
<img width="953" height="741" alt="image" src="https://github.com/user-attachments/assets/f4fc6bc1-92ad-47cd-9cb6-5b34d2111585" />
<img width="950" height="486" alt="image" src="https://github.com/user-attachments/assets/5cf36626-71f2-45fe-822e-4b034ef0781b" />

## LoadBalancer Service (Cloud External Access)
    In Kubernetes, a LoadBalancer Service is used to expose your application to the internet using a cloud provider’s load balancer
    A LoadBalancer Service:
            Creates an external IP
            Uses a cloud load balancer (AWS, Azure, GCP) 
            Automatically routes traffic to your Pods
<img width="949" height="503" alt="image" src="https://github.com/user-attachments/assets/4faf0a92-f272-413b-92a8-fd4d6e998ef1" />
The EXTERNAL-IP shows the public IP assigned by a cloud load balancer. It remains <pending> in local clusters because there is no cloud provider to provision the load balancer

## Understand the Service Types Side by Side
    ClusterIP is for internal communication
    NodePort exposes services via node IPs 
    LoadBalancer provides a cloud-managed public IP
<img width="1432" height="559" alt="image" src="https://github.com/user-attachments/assets/a29d85a9-a49d-4060-bd6a-4f6814a5ee88" />



















          
