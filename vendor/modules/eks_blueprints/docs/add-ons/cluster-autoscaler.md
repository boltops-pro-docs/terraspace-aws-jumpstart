<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/terraspace-aws-jumpstart/blob/master/vendor/modules/eks_blueprints/docs/add-ons/cluster-autoscaler.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

# Cluster Autoscaler

Cluster Autoscaler is a tool that automatically adjusts the number of nodes in your cluster when:

* Pods fail due to insufficient resources, or
* Pods are rescheduled onto other nodes due to being in nodes that are underutilized for an extended period of time.

The [Cluster Autoscaler](https://github.com/kubernetes/autoscaler/tree/master/cluster-autoscaler) add-on adds support for Cluster Autoscaler to an EKS cluster. It is typically installed as a **Deployment** in your cluster. It uses leader election to ensure high availability, but scaling is one done via one replica at a time.

## Usage

[Cluster Autoscaler](https://github.com/aws-ia/terraform-aws-eks-blueprints/tree/main/modules/kubernetes-addons/cluster-autoscaler) can be deployed by enabling the add-on via the following.

```hcl
enable_cluster_autoscaler = true
```

### GitOps Configuration

The following properties are made available for use when managing the add-on via GitOps.

```hcl
clusterAutoscaler = {
  enable = true
  serviceAccountName = "<service_account>"
}
```
