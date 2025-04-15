# DevOps-Challenge-

Terraform Configuration:
Designed modular infrastructure using Terraform HCL with three core files:
main.tf: Contains primary EKS cluster configuration with hardcoded values for this specific implementation
variables.tf: Defines all configurable parameters for infrastructure customization
outputs.tf: Exposes critical resource identifiers and endpoints




Kubernetes Deployment:
Implemented through dedicated manifest files:
Deployment: Manages pod lifecycle and container specifications
Service (LoadBalancer type): Provisions AWS ALB for external access
Horizontal Pod Autoscaler: Automatically scales pods between 1-3 replicas based on CPU/memory utilization



Application Packaging:
Containerized sample "Hello Kubernetes" application using Docker
Published built image to public DockerHub repository via CI/CD pipeline



Access Architecture:
End-users connect via AWS-provisioned Application Load Balancer
LoadBalancer service routes traffic to healthy pods across private subnets
Auto-scaling maintains performance during traffic spikes

##