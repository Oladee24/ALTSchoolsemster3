# ALTSchoolsemster3
innovativeeksretailstore


- Created `terraform/main.tf` on GitHub to define:
  - VPC (`innovatemart-vpc`) with public/private subnets.
  - EKS cluster (`innovatemart-eks`) with t3.medium nodes.
  - IAM user (`dev-readonly`) with read-only EKS/logs permissions.
- Created `terraform/outputs.tf` to output the EKS cluster endpoint.

- - Created `kubernetes/sample-pod.yaml` as a placeholder for the retail store app.
- (Optional) Uploaded full manifests from `aws-containers/retail-store-sample-app` for ui, orders, catalog, carts, and in-cluster databases (MySQL, PostgreSQL, DynamoDB Local, Redis, RabbitMQ).

- - Created `cicd/.github/workflows/terraform.yml` for GitHub Actions:
  - Runs `terraform plan` on pull requests.
  - Runs `terraform apply` on main branch pushes.
  - Uses GitHub Secrets for AWS credentials.
 
  - - Created `docs/guide.md` with:
  - Project overview and architecture.
  - Instructions for app access and developer IAM user.
  - GitHub repository link.
 
  - Added `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` to GitHub Secrets forthe CI/CD.
 
- Created `docs/guide.md` with:
  - Project overview and architecture.
  - Instructions for app access and developer IAM user.
  - GitHub repository link.
