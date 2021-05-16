# AWS Infrastructure 

## VPC
VPC with public and private subnets configured in three AZs,
three public and three private with NAT gateways in the public subnets.

## Image-Repository 
ECR repository which will hold the images for our
built application. We allow any users associated with this account to push/push to/from this repository. ECR are used in Fargate service tasks.

## ECS Cluster (Fargate cluster)
Fargate cluster that is in a VPC with private subnets. Containers can be deployed into the private subnets, and there are one load balancer which can be used to send traffic to the containers in the private subnet.

## ECS Service 
Which is responsible for task reliability and availability 

## Deployment pipeline
CICD Infrastructure to deploy latest image to fargate cluster service nodes. 

