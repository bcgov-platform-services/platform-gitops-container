# platform-gitops-container

Container Image for use with the Platform Registry and Cluster Configuration Manager (CCM) GitOps Pipelines

## Tools

| Name | Version | Description |
| :--- | :-----: | :---------- |
| Ansible   | 2.11.x | Ansible |
| Kubeseal  | 0.16.0 | Sealed secret management tool from bitnami. |
| Kustomize | 4.2.0 | Kubernets manifest templating system |
| OCP CLI   | 4.7.0-0 | OpenShift CLI from OKd |

## Usage

### Use with Github Actions

The container image used in GitHub Actions can be specified like this:

```yaml
jobs:
  build:
  generate:
    container: ghcr.io/bcgov-c/platform-gitops-container:v0.0.1
    runs-on: ubuntu-latest
```

### Use Locally

Coming Soon!

## Development

- Test Builds will be run when Pull Requests are created
- Merging to Main will build, push, and tag a release as `main`
- Creating a Release with a `v.X.Y.Z` tag will tag the image accordingly
- New Builds will take place every day at 3am

### Todo

- Update readme for local use
- Add HC Vault to container
- Create Tests for Pull Requests, and build latest on PR.
- Add Notifications for new base images, package upgrades including security patches, and new base images
- Switch to `pipenv` for better management of python dependencies
