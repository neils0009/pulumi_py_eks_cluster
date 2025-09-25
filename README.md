 # AWS EKS Cluster using pulumi

 ## Overview

 This project provosions EKS Kubernetes cluster inside a AWS VPC with proper NodeGroup and Networking Configured

 ## Prerequisites

 - An AWS account with permissions to create S3 buckets.
 - AWS credentials configured in your environment (for example via AWS CLI or environment variables).
 - Python 3.6 or later installed.
 - Pulumi CLI already installed and logged in.

 ## Outputs
- View Stack Output

  `pulumi stack output`

- Verify that the EKS cluster exists, by either using the AWS Console or running 

  `aws eks list-clusters`

- Update your KubeConfig, Authenticate to your Kubernetes Cluster and verify you have API access and nodes running.

  `aws eks --region <aws_region> update-kubeconfig --name $(pulumi stack output cluster-name)`

- check the Kubernetes Nodes

  `kubectl get nodes`