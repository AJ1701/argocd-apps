# authentication

## Inputs
|            Inpu       |     Type       | Description                                    |
|-----------------------|----------------|------------------------------------------------|
|identityName           |     String     | Name of the operator in the catalog            |
|clientID               |     String     | Namespace to deploy resources                  |
|clientSecretName       |     String     | Subscription data                              |
|clientSecretNamespace  |     String     | Destination namespaces for the operator        |
|organizationName       |     String     | Whether to create a namespace for the operator |

## Example
```
identityName: GitHub
clientID: ffbdf89185dabf5febaf
clientSecretName: github-oauth-credentials
clientSecretNamespace: openshift-config
organizationName: aj1701-demo-org
```