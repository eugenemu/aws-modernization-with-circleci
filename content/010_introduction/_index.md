---
title: "Introduction"
chapter: true
weight: 1
---

# Learning Objectives
Today we are going to learn the following topics:

- Deploy Cloud9 as an IDE for completing workshop exercises.
- Setting up project repositories in CircleCI
- Creating CI/CD pipelines and segments for:
    - Automated testing
    - Security scans (DevSecOps)
    - Building Docker images
    - Infrastructure as Code (IaC) using Terraform
    - Deploy applications
- Integrating the following services in CI/CD pipelines:
    - Snyk: app and container image scanning
    - AWS Public ECR: push Docker image to public AWS ECR repository
    - Terraform: codify and provision AWS resources and infrastructure 
    - Terraform Cloud: centrally manage state of provisioned infrastructure

# Workshop Structure

This workshop is broken into the sections listed below.  Estimated time for completing the workshop is 1.5-2.5 hours.

- **Prerequisites** ***(15 minutes)*** - Provision a Cloud9 instance and validate
- **Setting up CircleCI** ***(15 minutes)*** - collect access tokens from integrated services (AWS, GitHub, Terraform Cloud, Snyk), fork the project repo and set it up in CircleCI.
- **Module 1: Continuous Delivery** ***(30 minutes)***
- **Module 2: DevSecOps** ***(30 minutes)***
- **Module 3: Infrastructure as Code** ***(30 minutes)***
- **Module 4: Continuous Deployments** ***(30 minutes)***
