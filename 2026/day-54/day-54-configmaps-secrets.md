# Day-54 Challege
## Kubernetes ConfigMaps and Secrets
    In Kubernetes, ConfigMaps and Secrets are used to manage configuration data separately from your application code. This makes your apps more flexible and secure

## Create a ConfigMap from Literals
    Creating a ConfigMap from literals in Kubernetes means you directly pass key-value pairs via the command line (no YAML needed)
  <img width="748" height="884" alt="image" src="https://github.com/user-attachments/assets/5e4f859a-a02b-46fe-a9f8-907f537743e0" />

## Create a ConfigMap from a File
    Creating a ConfigMap from a file in Kubernetes is very common when you want to store full config files (like .conf, .json, .properties, etc.)
    You can mount a ConfigMap into a Pod. A file is created for each entry based on the key name
    The contents of that file set to the value
<img width="804" height="935" alt="image" src="https://github.com/user-attachments/assets/cd8bdf32-7317-4cab-9ae7-d013999a64a2" />

## Use ConfigMaps in a Pod
    Using a ConfigMap in a Pod is one of the most important Kubernetes skills
    Use env vars for simple configs and volume mounts for file-based configs like Nginx
<img width="1083" height="945" alt="image" src="https://github.com/user-attachments/assets/9100a178-012e-412b-b04a-f0fb091d8f72" />

## Create a Secret
    While ConfigMaps are great for most configuration data, there is certain data that is extra sensitive.
    This includes passwords, security tokens, or other types of private keys.
    Collectively, we call this type of data "Secret." Kubernetes has native support for storing and handling this data with care.
    Creating a Secret in Kubernetes is very similar to ConfigMaps, but used for sensitive data like passwords, tokens, etc.
<img width="1600" height="454" alt="image" src="https://github.com/user-attachments/assets/e6bda48e-0107-440d-b841-effe8f9c6e57" />

## Use Secrets in a Pod
    Using a Secret in a Pod is very similar to ConfigMaps, but for sensitive data like passwords, tokens, etc.
    Secrets can be injected into Pods as environment variables or mounted as files.
    Volumes are preferred for sensitive data like certificates.
