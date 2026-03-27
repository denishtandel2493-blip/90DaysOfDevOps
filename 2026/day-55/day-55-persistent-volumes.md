# Day-54 Challenge
## Persistent Volumes (PV) and Persistent Volume Claims (PVC)
    Persistent storage is critical in Kubernetes because Pods are ephemeral (they can be deleted anytime)
    That’s where Persistent Volumes (PV) and Persistent Volume Claims (PVC) come in
### Persistent Volumes
      A Persistent Volume is actual storage in the cluster
      Disk provided by the cluster Backed by:   Local disk, NFS, Cloud storage (AWS EBS, GCE PD, etc.)
### Persistent Volume Claims (PVC)
    A PVC is a request for storage. User asking for disk

## See the Problem — Data Lost on Pod Deletion
    Create a Simple pod manifest
    Create some data
    Delete the Pod
    Recreate Pod
    data disappear----- Because:Pod storage is ephemeral, Each Pod gets a new filesystem,
    When Pod is deleted → data is gone
<img width="778" height="605" alt="image" src="https://github.com/user-attachments/assets/9cb8939e-7e43-4916-8b06-4b805d3ccdc8" />

##  Create a PersistentVolume (Static Provisioning)
    Persistent Volume means, You manually create storage (PV) first
    Create PersistentVolume YAML
    Apply the PV ------  kubectl apply -f pv.yaml
    Check PV Status ------   kubectl get pv
     Is The STATUS of the PV?-----PV = Available
<img width="817" height="552" alt="image" src="https://github.com/user-attachments/assets/7b6f06f9-352c-4b15-af0e-1bd0cf4f8247" />

## 





                      
                        
