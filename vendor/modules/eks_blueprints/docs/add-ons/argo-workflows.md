<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/terraspace-aws-jumpstart/blob/master/vendor/modules/eks_blueprints/docs/add-ons/argo-workflows.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

# Argo Workflows

[Argo Workflows](https://argoproj.github.io/argo-workflows/) is an open source container-native workflow engine for orchestrating parallel jobs on Kubernetes. It is implemented as a Kubernetes CRD (Custom Resource Definition). As a result, Argo workflows can be managed using kubectl and natively integrates with other Kubernetes services such as volumes, secrets, and RBAC.

For complete project documentation, please visit the [Argo Workflows documentation site](https://argoproj.github.io/argo-workflows/).

## Usage

Argo Workflows can be deployed by enabling the add-on via the following.

```hcl
enable_argo_workflows = true
```


```

### GitOps Configuration

The following properties are made available for use when managing the add-on via GitOps.

```
argoWorkflows = {
  enable             = true
}
```
