# AWS Platform Template Standardisation Architecture

## 1. Application Deployment Architecture

```text
Developer
    |
    v
index.html
    |
    v
Dockerfile
    |
    v
Docker Image
    |
    v
Amazon ECR
    |
    v
Amazon ECS
    |
    v
AWS Fargate
    |
    v
Running Container
    |
    v
Nginx
    |
    v
Web Browser


Platform Standardisation Architecture

                     Platform Team
                         |
                         v
              Standard Platform Template
                         |
          +--------------+--------------+
          |                             |
          v                             v
   Infrastructure                 Application Inputs
   Configuration                  |
          |                        +-- Container Image
          |                        |
          |                        +-- Container Port
          |
          v
      AWS Fargate
          |
          v
      ECS Task
          |
          v
    Running Application


    Project Architecture

                             Git Repository
                              |
              +---------------+---------------+
              |                               |
              v                               v
        Application Code                Platform Templates
              |                               |
              v                               v
          Dockerfile                    CloudFormation
              |                               |
              v                               v
             ECR                         Standard Rules
              |                               |
              +---------------+---------------+
                              |
                              v
                         ECS Fargate
                              |
                              v
                        Web Application