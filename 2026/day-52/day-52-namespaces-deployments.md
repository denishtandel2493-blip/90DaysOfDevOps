# Day-52 Challenge
## Explore Default Namespaces
    Kubernetes does comes with built-in namespaces
    They are created automatically when a cluster is initialized and help organize and isolate resources
    Default :-  This is where your resources go if you don’t specify a namespace
    
    kube-system :-  Used by Kubernetes Internal Components, Contains core components like:
    DNS (CoreDNS), kube-apiserver, scheduler, You usually don’t touch this namespace
    
    kube-public :- Accessible to all users (even unauthenticated in some setups)
    Used for publicly readable cluster info. Rarely used manually

    kube-node-lease:-  Stores node heartbeat info. Helps Kubernetes track node availability efficiently.
    Improves cluster performance.
<img width="1500" height="499" alt="image" src="https://github.com/user-attachments/assets/76c5d5d4-baee-40a6-bb59-7ba7703972f2" />
show many pod are running in kube-system

## Create and Use Custom Namespaces
    Creating and using custom namespaces in Kubernetes is a core skill—especially for DevOps setups like dev / staging / prod separation
    kubectl get pods shows pods in the current namespace, while kubectl get pods -A shows pods in all namespaces
<img width="1208" height="802" alt="image" src="https://github.com/user-attachments/assets/90bae6f3-6ba5-4799-99b8-8c68d594fe56" />

## Create Your First Deployment
    A Kubernetes Deployment is a tool that runs and keeps your app (pods) alive automatically, and lets you scale or update it easily
<img width="934" height="981" alt="image" src="https://github.com/user-attachments/assets/21cf4feb-7ae5-4c30-9547-14d8ca0b625e" />

## Self-Healing — Delete a Pod and Watch It Come Back
    If you delete a Pod, the Deployment automatically creates a new one to replace it
    The deleted pod is replaced within seconds,  pod's name is the Different
<img width="897" height="936" alt="image" src="https://github.com/user-attachments/assets/1305f832-ef70-4442-a09e-dd6d756c920f" />

## Scale the Deployment
    Scaling a Deployment means changing how many Pods (copies of your app) are running
    When you scaled down from 5 to 2, the extra pods is removed
<img width="1674" height="683" alt="image" src="https://github.com/user-attachments/assets/e87753df-651a-40f5-b39e-5ac647bd8408" />

##  Rolling Update
    Update your app without downtime by replacing old Pods one by one with new ones
    Old Pods are gradually terminated
    New Pods are created with new version
    App stays running the whole time (no downtime)
<img width="1267" height="544" alt="image" src="https://github.com/user-attachments/assets/fe8d1205-6519-4da3-94ed-616a63a62517" />

## Clean Up
    kubectl delete deployment nginx-deployment -n dev
    kubectl delete pod nginx-dev -n dev
    kubectl delete pod nginx-staging -n staging
    kubectl delete namespace dev staging production
<img width="1263" height="762" alt="image" src="https://github.com/user-attachments/assets/27bd013f-aeae-493a-b58c-7bc2d90d2e58" />



        
      
      


