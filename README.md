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

## Architecture

graph TD
    A[Terraform] --> B[AWS Infrastructure]
    B --> C[EKS Cluster]
    B --> D[VPC Network]
    B --> E[IAM Roles]
    C --> F[Worker Nodes]
    C --> G[OpenTelemetry Demo]
    G --> H[Frontend Service]
    G --> I[Backend Services]
    G --> J[Observability Stack]
    J --> K[Prometheus]
    J --> L[Grafana]
    J --> M[Jaeger]
    K --> N[AWS SNS Alerts]


    flowchart LR
    App-->|Traces|Jaeger
    App-->|Metrics|Prometheus
    Prometheus-->Grafana
    Prometheus-->|Alerts|SNS-->Email
