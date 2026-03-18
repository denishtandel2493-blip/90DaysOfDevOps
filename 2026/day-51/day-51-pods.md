# Day-51 Challenge
## Create Your First Pod (Nginx)
    Create a file called nginx-pod.yaml
<img width="1250" height="1004" alt="image" src="https://github.com/user-attachments/assets/dfef0a00-31dc-4a48-9af0-a07de11ee3ef" />
<img width="1288" height="837" alt="image" src="https://github.com/user-attachments/assets/3f98f3f0-7aab-40fa-b43b-3607584a6ef5" />
<img width="1590" height="1016" alt="image" src="https://github.com/user-attachments/assets/b3dc6eb5-de29-4bcc-a3f5-2e3c41f2b642" />
    yes, I have see the Nginx welcome page when you curl from inside the pod

## Create a Custom Pod (BusyBox)
        Write a new manifest busybox-pod.yaml
<img width="913" height="583" alt="image" src="https://github.com/user-attachments/assets/46a18c82-cedd-41c1-a5e2-58ca1e494541" />
If no command is provided, Kubernetes uses the image’s default CMD. If that process exits immediately, the container enters CrashLoopBackOff

##  Imperative vs Declarative
     Imperative commands directly execute actions (like kubectl run), while declarative uses YAML to define desired state and Kubernetes ensures it. 
     Declarative is preferred for production because it is version-controlled and reproducible.
### Declarative Approach
        You define desired state in a YAML file, and Kubernetes makes it happen.
        # kubectl apply -f pod.yml
        
    apiVersion: v1
    kind: Pod
    metadata:
      name: nginx-pod
    spec:
      containers:
      - name: nginx
        image: nginx
### Imperative Approach
        You directly give commands to Kubernetes
        # kubectl run redis-pod --image=redis:latest
<img width="1375" height="1004" alt="image" src="https://github.com/user-attachments/assets/8fab9028-09da-46a2-82ef-387b042b3d46" />
            
            Compare this output with your hand-written manifests. Notice how much extra metadata Kubernetes adds automatically (status, timestamps, uid, resource version).    
<img width="1483" height="981" alt="image" src="https://github.com/user-attachments/assets/52b057c4-0c5e-4206-b3a6-76e7f49a76b3" />
        
        Dry-run generates a minimal manifest with default values, while manual YAML is customized. The main differences are labels, container naming, and missing optional fields like ports. Kubernetes also adds runtime metadata when retrieving live objects.”
<img width="1305" height="378" alt="image" src="https://github.com/user-attachments/assets/0a2d9ccf-0229-42f0-97f1-78c24f44e27e" />

## Validate Before Applying
        Validation can be done using --dry-run=client for syntax and --dry-run=server for full API validation. 
        This ensures the manifest is correct before applying it to the cluster.
<img width="1173" height="428" alt="image" src="https://github.com/user-attachments/assets/51f8b0e4-4ceb-4dff-9e93-ea8bc287aae4" />
         
    What error does Kubernetes give when the image field is missing?
    The Pod "nginx-pod" is invalid: spec.containers[0].image: Required value

## Pod Labels and Filtering
        Labels are key-value pairs used to organize and select Kubernetes resources. 
        They are used by Services and controllers to identify target pods.
<img width="926" height="976" alt="image" src="https://github.com/user-attachments/assets/5b5ccc54-ed33-452f-a863-9d2c8daa6634" />

##  Clean Up
        Delete all the pods you created
<img width="925" height="731" alt="image" src="https://github.com/user-attachments/assets/efbcc6fd-cefe-44ee-b69b-49cf3df00972" />
        
        A standalone pod is not managed by any controller, so when it is deleted, Kubernetes does not recreate it. 
        Controllers like Deployments ensure pods are recreated automatically









        
