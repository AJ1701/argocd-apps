# authentication

## Prerequisites
- Configure [GitHub application on GitHub.com](https://docs.openshift.com/container-platform/4.6/authentication/identity_providers/configuring-github-identity-provider.html#identity-provider-registering-github_configuring-github-identity-provider)
- [Create a secret for the client secret](https://docs.openshift.com/container-platform/4.6/authentication/identity_providers/configuring-github-identity-provider.html#identity-provider-creating-secret_configuring-github-identity-provider)

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