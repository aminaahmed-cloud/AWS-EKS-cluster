# AWS-EKS-cluster with EKSCTL command line tool

EKSCTL is a Command Line Tool for working with EKS clusters that automates many individual tasks.

## EKSCTL Benefits

- Execute just one command
- Necessary components get created and configured in the background
- Cluster will be created with default parameters
- With more CLI options, you can customize your cluster

---

## Installation

First, download the eksctl command line tool with your AWS account.

```bash
% brew tap weaveworks/tap
% brew install weaveworks/tap/eksctl
```

---

## Configure AWS Credentials

Ensure your AWS credentials are properly configured.

```
% aws configure list
```

---

## Create EKS Cluster

Use eksctl to create your EKS cluster.

```
% eksctl create cluster \
--name demo-cluster \
--version 1.27 \
--region eu-west-2 \
--nodegroup-name demo-nodes \
--node-type t2.micro \
--nodes 2 \
--nodes-min 1 \
--nodes-max 3
```

This command creates an EKS cluster named "demo-cluster" with Kubernetes version 1.27 in the "eu-west-2" region. It also creates a node group named "demo-nodes" with EC2 instance type "t2.micro", consisting of 2 nodes with a minimum of 1 and a maximum of 3 nodes

<img src="https://i.imgur.com/Oqu5iAX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

