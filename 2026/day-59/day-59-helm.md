## Helm --- kubernetes package manager
    Helm is a tool that helps you manage Kubernetes applications easily using reusable templates called charts
    Helm = package manager for Kubernetes Just like: apt for Ubuntu, yum for CentOS  
    Helm helps you install, upgrade, and manage apps in Kubernetes with one command instead of writing long YAML files

## Helm Install
    Install Helm on Linux (Ubuntu)
        # curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash
    Three core concepts:
      1. Chart :- A Chart is a package of Kubernetes YAML files - Deployment -  Service -  ConfigMap
                  A package of Kubernetes manifest templates
      2. Release :- A Release is a running instance of a chart in your cluster. Every install creates a release
                    Can have multiple releases of same chart
                    A specific installation of a chart in your cluster
      3. Repository :- A Repository is a place where charts are stored. Like Docker Hub but for Helm charts, You download charts from here
                      A collection of charts (like a package repo)
<img width="886" height="761" alt="image" src="https://github.com/user-attachments/assets/38593ffb-73bb-40f9-9632-ad3c7ae18f55" />

## Add Repository and Search
    Add the Bitnami repository: helm repo add bitnami https://charts.bitnami.com/bitnami
    Downloads latest chart list from all repos
    Update: helm repo update
    First add and update repository, then search and install charts
    Bitnami has more than 100 production-ready Helm charts
<img width="1345" height="984" alt="image" src="https://github.com/user-attachments/assets/231eb697-a9d4-4b18-ab1f-206e552a012d" />

## Install a chart
    Helm simplifies Kubernetes deployments by packaging multiple resources into a single chart, allowing deployment with one command instead of multiple YAML files
<img width="1702" height="983" alt="image" src="https://github.com/user-attachments/assets/5251d483-b068-4233-8304-4ce392438f28" />
<img width="1472" height="987" alt="image" src="https://github.com/user-attachments/assets/fba37dd5-003f-4798-bf6a-54e65f6af634" />
<img width="1271" height="981" alt="image" src="https://github.com/user-attachments/assets/2332613d-f54a-4005-bddb-074cde3e9c1a" />

