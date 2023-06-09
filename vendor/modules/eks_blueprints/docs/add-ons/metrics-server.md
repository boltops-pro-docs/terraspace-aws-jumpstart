<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/terraspace-aws-jumpstart/blob/master/vendor/modules/eks_blueprints/docs/add-ons/metrics-server.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

# Metrics Server

Metrics Server is a scalable, efficient source of container resource metrics for Kubernetes built-in autoscaling pipelines. It is not deployed by default in Amazon EKS clusters. The Metrics Server is commonly used by other Kubernetes add-ons, such as the Horizontal Pod Autoscaler, Vertical Autoscaling or the Kubernetes Dashboard.

> **Important**: Don't use Metrics Server when you need an accurate source of resource usage metrics or as a monitoring solution.

## Usage

[Metrics Server](https://github.com/aws-ia/terraform-aws-eks-blueprints/tree/main/modules/kubernetes-addons/metrics-server) can be deployed by enabling the add-on via the following.

```hcl
enable_metrics_server = true
```

Once deployed, you can see metrics-server pod in the `kube-system` namespace.

```sh
$ kubectl get deployments -n kube-system

NAME                                                          READY   UP-TO-DATE   AVAILABLE   AGE
metrics-server                                                1/1     1            1           20m
```

### GitOps Configuration

The following properties are made available for use when managing the add-on via GitOps

```
metricsServer = {
  enable = true
}
```
