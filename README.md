# 🚀 Secure CI/CD for Java App using GitHub OIDC & AWS ECR

## 📦 Pipeline Flow
1. GitHub pushes trigger workflow.
2. GitHub Actions assumes AWS IAM role via OIDC.
3. Multi-stage Docker image is built.
4. Image is pushed to AWS ECR.

## 🐳 Multi-stage Docker Build
- **Stage 1:** Build JAR using Maven.
- **Stage 2:** Use OpenJDK Alpine to run JAR.

## 🔐 AWS IAM Role for OIDC
```json
"sub": "repo:yourname/yourrepo:ref:refs/heads/main"
