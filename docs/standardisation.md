# Platform Template Standardisation

## Objective

The objective of this study is to understand how platform
templates can standardize the deployment configuration used
by application teams.

## Problem with Manual Deployment

In a manual deployment, developers or administrators must
configure infrastructure settings individually.

Examples include:

- ECS cluster configuration
- Fargate compute settings
- Memory allocation
- Container port
- Container image
- IAM execution role
- Networking
- Security group configuration

Repeated manual configuration can introduce inconsistencies
between deployments.

## Standardisation Approach

A reusable infrastructure template can define common
platform requirements once.

Application-specific values can then be supplied as inputs.

Conceptually:

Developer Application
        |
        v
Standard Platform Template
        |
        v
Reusable Infrastructure Configuration
        |
        v
AWS Resources

## Standard Configuration

The study uses the following baseline configuration:

| Configuration | Standard Value |
|---|---|
| Compute | AWS Fargate |
| CPU | 256 |
| Memory | 512 MiB |
| Network Mode | awsvpc |
| Container Port | Application supplied |
| Execution Role | ecsTaskExecutionRole |
| Container Image | Application supplied |

## Reusable Inputs

The template accepts application-specific values such as:

### Container Image

The Docker image can be supplied by the application team.

Example:

```text
629845797142.dkr.ecr.ap-south-1.amazonaws.com/aws-proton-demo:latest