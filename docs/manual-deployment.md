# Manual Deployment Baseline

## Overview

The application was first deployed manually using Amazon ECS
with AWS Fargate.

The purpose of this deployment was to establish a working
baseline before studying infrastructure standardisation.

## Deployment Flow

Developer
    ↓
HTML Application
    ↓
Docker Image
    ↓
Amazon ECR
    ↓
Amazon ECS
    ↓
AWS Fargate
    ↓
Running Web Application

## AWS Configuration

| Component | Configuration |
|---|---|
| Region | ap-south-1 |
| Container Platform | AWS Fargate |
| ECS Cluster | aws-proton-cluster |
| Task Definition | aws-proton-demo-task |
| CPU | 256 |
| Memory | 512 MiB |
| Container Port | 80 |
| Container | aws-proton-demo-container |
| Image Registry | Amazon ECR |
| Web Server | Nginx |

## Manual Steps

1. Created the web application.
2. Created a Dockerfile.
3. Built the Docker image.
4. Created an Amazon ECR repository.
5. Pushed the Docker image to ECR.
6. Created an ECS Fargate cluster.
7. Created an ECS task definition.
8. Created an ECS service.
9. Configured networking and security group rules.
10. Assigned a public IP to the running task.
11. Verified the application through a web browser.

## Result

The application was successfully deployed and accessed
through the public IP address of the Fargate task.

## Limitation of Manual Configuration

Manual deployment requires the platform configuration to be
entered repeatedly.

This can result in:

- configuration inconsistencies
- repeated setup work
- human errors
- difficulty maintaining common standards
- increased onboarding effort for developers

This baseline is therefore used to study how reusable
platform templates can standardize infrastructure configuration.