# AWS Platform Template Standardisation

## Deployment Architecture

Developer
   ↓
index.html
   ↓
Dockerfile
   ↓
Docker Image
   ↓
Amazon ECR
   ↓
Amazon ECS Fargate
   ↓
ECS Service
   ↓
Running Container
   ↓
Web Application

## AWS Resources

- AWS Region: Asia Pacific (Mumbai)
- Region Code: ap-south-1
- ECS Cluster: aws-proton-cluster
- ECS Task Definition: aws-proton-demo-task
- Task Definition Revision: 1
- ECS Service: aws-proton-demo-task-service
- Launch Type: AWS Fargate
- CPU: 0.25 vCPU
- Memory: 512 MiB
- Container Port: 80
- Container: aws-proton-demo-container
- Container Image: Amazon ECR
- Web Server: Nginx

## Deployment Status

The application was successfully packaged as a Docker container,
stored in Amazon ECR, and deployed using Amazon ECS Fargate.

## Purpose

This deployment represents the manual baseline for the
AWS Platform Template Standardisation study.

The next stage will investigate how standardized infrastructure
templates can reduce repeated configuration and improve
consistency across application deployments.