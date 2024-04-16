### EKS Cluster 생성

```bash
CLUSTER_NAME=<cluster-name>
AWS_ACCOUNT_ID=$(aws sts get-caller-identity --query "Account" --output text)
AWS_REGION=ap-northeast-2
eksctl create cluster --name $CLUSTER_NAME --region ap-northeast-2 --version 1.29 --node-private-networking --nodes-max=10
```
