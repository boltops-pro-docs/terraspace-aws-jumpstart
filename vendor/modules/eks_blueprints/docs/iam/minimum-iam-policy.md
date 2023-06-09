<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/terraspace-aws-jumpstart/blob/master/vendor/modules/eks_blueprints/docs/iam/minimum-iam-policy.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

# Minimum IAM policy

This document describes the minimum IAM policy required to run [core examples](https://github.com/aws-ia/terraform-aws-eks-blueprints/blob/main/.github/workflows/e2e-parallel-full.yml#L30-L47) that we run in our [E2E workflow](https://github.com/aws-ia/terraform-aws-eks-blueprints/blob/main/.github/workflows/e2e-parallel-full.yml) , mainly focused on the list of IAM actions.

> **Note**: The policy resource is set as `*` to allow all resources, this is not a recommended practice.

~~~yaml
{% include "min-iam-policy.json" %}
~~~

## How this policy was generated?

For each example we run in the E2E workflow, we run [iamlive](https://github.com/iann0036/iamlive) in the background in CSM mode to help generate the policy.  
After generating the policy for each example, we merge the generated policies into a single policy shown above.

To learn more about the implementation you can review the [GitHub workflow itself](https://github.com/aws-ia/terraform-aws-eks-blueprints/blob/main/.github/workflows/e2e-parallel-full.yml)
