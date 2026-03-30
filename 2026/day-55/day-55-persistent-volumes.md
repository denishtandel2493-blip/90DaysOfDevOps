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

## Create a PersistentVolumeClaim
    The VOLUME column shows the name of the PersistentVolume that the PVC is bound to
<img width="881" height="818" alt="image" src="https://github.com/user-attachments/assets/85d9d295-c564-4c50-a11b-899e7bd6836b" />

## Use the PVC in a Pod — Data That Survives
    prove that data survives even after Pod deletion using your PVC
    PVC decouples storage from Pod lifecycle, so data survives Pod deletion
    Pod deleted → data NOT lost------- New Pod → same data available
    Does the file contain data from both the first and second Pod?  Yes — the file contains the same data written by the first Pod, and it is available to the second Pod.
<img width="883" height="938" alt="image" src="https://github.com/user-attachments/assets/826609fa-af9a-4746-9a89-8568f5ae5056" />

## StorageClasses and Dynamic Provisioning
    Kubernetes automatically creates PV when PVC is created
    A StorageClass defines: Type of storage (SSD, HDD, cloud disk) 
                            Provisioner (who creates storage)
                            Parameters (size, performance, etc.)
    Default StorageClass is used automatically if PVC doesn’t specify one
<img width="883" height="897" alt="image" src="https://github.com/user-attachments/assets/dcc92df0-c588-4c39-810a-6a53d5dbbe59" />






                      
                        
