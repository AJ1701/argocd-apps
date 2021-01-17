# cluster-applications

## Prerequisites
- ArgoCD Installed

## Deploying via App of Apps
Simply create an ArgoCD application resource in this directory to have ArgoCD deploy your application.

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