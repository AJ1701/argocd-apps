# cluster-applications

## Deploying via App of Apps
Simply create an ArgoCD application resource in this directory to have ArgoCD deploy your application. Create a new directory with the static manifests, helm, kustomize, ksonnet, or jsonnet contained within.

## Application Resource Documentation
https://argoproj.github.io/argo-cd/operator-manual/declarative-setup/#applications

## Example
```
apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: guestbook
  namespace: argocd
spec:
  project: default
  source:
    repoURL: https://github.com/argoproj/argocd-example-apps.git
    targetRevision: HEAD
    path: guestbook
  destination:
    server: https://kubernetes.default.svc
    namespace: guestbook
```