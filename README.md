# end to end React Application GitOps Repository

## GitHub as the Single Source of Truth

This project follows the GitOps principle of treating GitHub as the single source of truth for the desired state of the application. Argo CD continuously monitors this repository and reconciles the Kubernetes cluster with the state defined in Git.

This repository contains the Kubernetes manifest files used to deploy the React application to a K3s Kubernetes cluster.


## Files

```text
end_to_end_react_gitops/
├── deployment.yaml
├── service.yaml
└── ingress.yaml

- deployment.yaml
Defines the React application Deployment and container image.

- service.yaml
Exposes the React application inside the Kubernetes cluster.

- ingress.yaml
Configures Traefik Ingress to expose the application through: http://react.local

GitOps Workflow
Jenkins
   |
   | Update Docker image version
   v
GitHub GitOps Repository
   |
   v
Argo CD
   |
   v
K3s
