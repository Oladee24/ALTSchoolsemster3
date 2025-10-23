
guide.md
 InnovateMart Project Bedrock Deployment Guide

 Overview
This project sets up an Amazon EKS cluster with a VPC using Terraform. The retail-store-sample-app is deployed with in-cluster databases (MySQL, PostgreSQL, DynamoDB Local, Redis, RabbitMQ). A CI/CD pipeline automates Terraform deployment. A read-only IAM user allows developers to view resources.

 Architecture
- **VPC**: `innovatemart-vpc` with 2 public and 2 private subnets.
- **EKS**: Cluster `innovatemart-eks` with t3.medium nodes.
- **App**: Retail store app (ui, orders, catalog, carts) with in-cluster databases.
- **CI/CD**: GitHub Actions runs `terraform plan` on pull requests and `apply` on main branch merge.
- **IAM**: User `dev-readonly` with read-only EKS/logs access.

Access Instructions
- **App**: Run:
