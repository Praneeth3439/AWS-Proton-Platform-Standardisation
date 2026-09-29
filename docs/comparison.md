# Manual Deployment vs Platform Standardisation

## Purpose

This comparison shows how the project changes when common
infrastructure configuration is represented as reusable
platform templates.

## Comparison

| Area | Manual Deployment | Standardised Template |
|---|---|---|
| ECS configuration | Configured manually | Defined in template |
| Fargate launch type | Selected manually | Defined by platform |
| CPU | Entered manually | Standard value |
| Memory | Entered manually | Standard value |
| IAM execution role | Selected manually | Defined by platform |
| Container image | Entered during deployment | Supplied as an input |
| Container port | Configured manually | Supplied as an input |
| Networking | Configured manually | Can be standardized |
| Repeatability | Depends on operator | Template-driven |
| Version control | Console configuration | Template files in Git |
| Developer responsibility | Higher | Lower |
| Platform team responsibility | Lower | Higher |

## Manual Deployment

The manual deployment performed in this project involved:

1. Building the Docker image.
2. Creating an ECR repository.
3. Pushing the image.
4. Creating an ECS cluster.
5. Creating a Fargate task definition.
6. Creating an ECS service.
7. Configuring networking.
8. Configuring security-group access.
9. Verifying the running application.

## Standardised Deployment Concept

The template approach separates:

### Platform-owned configuration

- Fargate
- CPU
- Memory
- Network mode
- IAM execution role
- Infrastructure structure

### Application-owned configuration

- Container image
- Container port
- Application code

This separation allows developers to focus more on their
application while the platform team maintains common
infrastructure standards.

## Version Control

The template files are stored in Git.

This provides:

- Change history
- Reviewable infrastructure changes
- Reproducibility
- Collaboration
- Versioned platform standards

## Key Learning

The main lesson from this study is that infrastructure
standardisation is not simply about automating deployment.

It is about defining a common platform configuration that can
be reused while allowing applications to provide only the
values that are specific to them.