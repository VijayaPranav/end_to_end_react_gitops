# end to end React Application GitOps Repository

This repository contains the Kubernetes manifest files used to deploy the React application to a K3s Kubernetes cluster.

Argo CD uses this repository as the single source of truth for the desired Kubernetes state.

## Files

```text
end_to_end_react_gitops/
├── deployment.yaml
├── service.yaml
└── ingress.yaml
