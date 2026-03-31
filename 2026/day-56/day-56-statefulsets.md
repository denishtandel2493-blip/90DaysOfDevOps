# Day-55 Challenge
## Kubernetes StatefulSets
    A StatefulSet is used to manage stateful applications like:
                Databases (MySQL, PostgreSQL, MongoDB)
                Kafka, Redis
                Any app needing stable identity + storage
    StatefulSet gives each Pod:
               Stable names
               Stable network identity
               Dedicated storage per Pod
    StatefulSets manage stateful applications by providing stable identities, ordered deployment, and persistent storage per Pod
<img width="886" height="985" alt="image" src="https://github.com/user-attachments/assets/8dec2d31-5135-4b5e-ac94-7f4c25433d6f" />
Random pod names are a problem because database clusters require stable identities for replication, storage mapping, and consistent communication between nodes

## Create a Headless Service
      This is the foundation for StatefulSets
        A Headless Service is a Service without a ClusterIP.
        Instead of load balancing, it:
            Exposes individual Pod DNS names
            Enables direct Pod-to-Pod communication
      A Headless Service (clusterIP: None) exposes individual Pod IPs and enables stable DNS, which is required for StatefulSets
<img width="836" height="518" alt="image" src="https://github.com/user-attachments/assets/8821e2ac-62c3-466f-b4fb-82137e46b06c" />

## Create a StatefulSet
    StatefulSet manages stateful applications by ensuring stable Pod identity, ordered deployment, and persistent storage
<img width="1508" height="944" alt="image" src="https://github.com/user-attachments/assets/4bd9d02d-e8ed-4627-8c07-281d067114bf" />

## Stable Network Identity
    Stable network identity means each Pod in a StatefulSet gets a fixed hostname and DNS that does not change, even if the Pod is restarted
    


