# Flask Kubernetes Deployment

This project demonstrates deploying a simple Flask web application to a Kubernetes cluster using minikube.

## Prerequisites

- Docker Desktop installed and running
- minikube installed
- kubectl installed 

## Getting Started

1. Start the minikube cluster:
  minikube start --driver=docker

3. Build the Flask Docker image:
  docker build -t myimage .


4. Apply the Kubernetes deployment and service:
  kubectl apply -f deployment.yaml -f service.yaml


5. Port forward to access the app:
  kubectl port-forward service/my-service 5000:5000


6. Access the running app at http://localhost:5000

## Cleanup
kubectl delete deployment my-deployment
kubectl delete service my-service
minikube stop


## Next Steps

- Configure CI/CD workflows
