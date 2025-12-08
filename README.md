# k8s-config

Repository configuration for Kubernetes clusters managed by ArgoCD.

## Directory Structure

*   **applications/**: ArgoCD Application definitions.
*   **manifests/**: Kubernetes manifests (Deployments, Services, Ingress, etc.).
    *   **testing/**: Testing environment configurations.
    *   **production/**: Production environment configurations.
*   **argocd/**: ArgoCD specific configurations (e.g., custom images, plugins).


## Usage

This repository is watched by ArgoCD to sync the desired state to the Kubernetes clusters.
