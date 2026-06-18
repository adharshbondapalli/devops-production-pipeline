# DevOps Production Pipeline

End-to-end DevOps project demonstrating a production-grade CI/CD pipeline
for a Java Spring Boot application.

## Tech Stack
- **CI/CD:** Jenkins (Declarative Pipeline)
- **Containerization:** Docker, Amazon ECR
- **Infrastructure:** Terraform, AWS (EC2, EKS, VPC, IAM)
- **Configuration Management:** Ansible
- **Orchestration:** Kubernetes (EKS)
- **Monitoring:** Prometheus, Grafana, AlertManager

## Pipeline Flow
Code Push → GitHub Webhook → Jenkins → Docker Build
→ ECR Push → Terraform Infra → K8s Deploy → Prometheus + Grafana

## Environments
| Environment | Branch | Purpose |
|---|---|---|
| dev | develop | Active development |
| staging | staging | Pre-production testing |
| prod | main | Live production |
