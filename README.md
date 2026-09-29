# AWS Platform Template Standardisation Study

## Overview

This project studies how reusable platform templates can
standardize cloud infrastructure deployment for application
teams.

The project first establishes a working manual deployment using
Docker, Amazon ECR, Amazon ECS, and AWS Fargate.

A reusable infrastructure template is then created to study
platform standardisation.

## Objectives

- Deploy a containerized web application on AWS.
- Understand Amazon ECS and AWS Fargate.
- Store Docker images in Amazon ECR.
- Study infrastructure standardisation.
- Create reusable infrastructure template files.
- Separate platform-owned configuration from application inputs.
- Version infrastructure templates using Git.
- Study AWS Proton as a platform-template approach.
- Consider modern alternatives for future deployments.

## Architecture

```text
Developer
    |
    v
Application Code
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
Running Web Application

Platform Standardisation

Platform Team
      |
      v
Standard Platform Template
      |
      +-----------------------+
      |                       |
      v                       v
Infrastructure Rules    Application Inputs
                              |
                              +-- Container Image
                              |
                              +-- Container Port