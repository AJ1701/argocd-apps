# operators

## Inputs
|                Input          |     Type       | Description                                    |
|-------------------------------|----------------|------------------------------------------------|
|metadata.operatorName          |     String     | Name of the operator in the catalog            |
|metadata.namespace             |     String     | Namespace to deploy resources                  |
|subscription                   |      Map       | Subscription data                              |
|operatorGroupNamespaces        |     List       | Destination namespaces for the operator        |
|createNamespace                |     Boolean    | Whether to create a namespace for the operator |

## Example
```
operators:
  - metadata:
      operatorName: argocd-operator
      namespace: argocd
    subscription: 
      channel: alpha
      installPlanApproval: Automatic
      name: argocd-operator
      source: community-operators
      sourceNamespace: openshift-marketplace
    operatorGroupNamespaces: 
      - argocd
    createNamespace: false
```