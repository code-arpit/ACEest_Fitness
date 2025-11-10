# Deployment Instructions

## Prerequisites
- Docker installed
- Kubernetes cluster (Minikube or cloud)
- kubectl CLI configured
- Docker Hub account for container images

## Steps
- Build Docker image:
    - docker build -t localhost/aceest_fitness:1.1.1 .

- Push Docker image to local registry:
    - docker push localhost/aceest_fitness:1.1.1

- Deploy to Kubernetes:
    - kubectl apply -f cluster/deployments/deployment.yaml
    - kubectl apply -f cluster/deployments/service.yaml

- For Canary Deployment:
    - Deploy stable and canary versions simultaneously.
    - Adjust replica counts for traffic distribution.
    - Deployment files can be found inside cluster/deployments directory

- For Blue-Green Deployment:
    - Deploy blue and green environments.
    - Switch service selector labels to change active environment.
    - Deployment files can be found inside cluster/deployments directory

- Monitor deployment and roll back if needed.
