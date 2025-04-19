# otel-eks-terraform

# OpenTelemetry on EKS (Terraform)

## Overview
A Terraform project that automatically provisions an AWS EKS cluster and deploys the OpenTelemetry demo application with full observability tooling.

## Key Components
| Component          | Technology Used       | Purpose                          |
|--------------------|-----------------------|----------------------------------|
| Infrastructure     | Terraform + AWS EKS   | Automated cluster provisioning   |
| Application        | Helm + OpenTelemetry  | Demo app deployment              |
| Monitoring        | Prometheus + Grafana  | Metrics collection/visualization |
| Alerting          | AWS SNS               | Email notifications              |
| CI/CD             | GitHub Actions        | Automated deployments           |

