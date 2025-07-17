------------------------------------------------------------------------------------------------
1) create this two clusters use this command with eksctl  

 eksctl create cluster   --name react-node-cluster   --version 1.29   --region ap-south-1  \
 --nodegroup-name react-node-workers   \
 --node-type t3.medium   --nodes 2   --nodes-min 1   --nodes-max 3   --managed

-----------------------------------------------------------------------------------------------
 2) To delete the cluster

eksctl delete cluster --name react-node-cluster --region ap-south-1

-----------------------------------------------------------------------------------------------
3) Create this two repos in the AWS

aws ecr create-repository --repository-name react-node-backend

aws ecr create-repository --repository-name react-node-frontend

----------------------------------------------------------------------------------------------

4) To delete the repos from AWS

aws ecr delete-repository \
  --repository-name react-node-backend \
  --region ap-south-1 \
  --force

aws ecr delete-repository \
  --repository-name react-node-frontend \
  --region ap-south-1 \
  --force
...
-----------------------------------------------------------------------------------------------

5) To authenticate the ECR with the machine


