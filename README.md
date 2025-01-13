# CI/CD Kubernetes Manifests

This repository contains Kubernetes manifests (YAML files) for deploying and managing applications in a Kubernetes cluster. The manifests are designed to work in a CI/CD pipeline and are monitored and applied to the cluster using **ArgoCD**.

---



## Overview

The **`cicd-k8s-manifests`** repository maintains declarative configurations for Kubernetes resources, including deployments, services, and other application components. These configurations ensure consistency and ease of deployment in Kubernetes environments.

### Key Features:
- **Deployment**: Configuration for deploying containerized applications.
- **Service**: Exposes the application to internal or external traffic.
- **ArgoCD Integration**: Enables automated and continuous synchronization of the manifests with the Kubernetes cluster.
- **Scalable**: Supports scaling and updating of applications in real-time.

---


## ArgoCD Integration

ArgoCD is used to monitor and synchronize the manifests in this repository with the Kubernetes cluster. Below are the key steps for integrating with ArgoCD:


1. **Continuous Deployment**:
   - Any updates to the manifests in this repository are automatically detected by ArgoCD.
   - ArgoCD ensures the Kubernetes cluster state matches the desired state defined in this repository.

2. **Sync and Monitor**:
   - Use the ArgoCD dashboard to monitor application health and deployment status.

---

## Manifests

### Deployment
The `deployment.yaml` file defines the following:
- The number of replicas for your application.
- The Docker image and tag used for the application.
- Resource requests and limits.

### Service
The `service.yaml` file defines:
- How the application is exposed (ClusterIP, NodePort, or LoadBalancer).
- Ports and protocols used by the application.


---

## How to Use

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/DarylAdrien/cicd-k8s-manifests.git
   cd cicd-k8s-manifests
   ```

2. **Modify Manifests**:

    Update the deployment.yaml file with your container image and environment-specific settings.
    Adjust the service.yaml file to match your application's network requirements.

3.**Commit and Push**:
  ```bash
  git add .
  git commit -m "Updated manifests"
  git push origin main
  ```

4.**ArgoCD Synchronization**:

  ArgoCD will automatically detect changes and synchronize the cluster.


---

## License

This project is licensed under the MIT License.
