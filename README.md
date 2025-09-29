# MyApp Kubernetes Deployment

This repository contains Kubernetes manifests to deploy and expose a simple Nginx application.

## Files

- [deployment.yaml](c:\Users\prata\OneDrive\Desktop\t5\deployment.yaml): Defines a Deployment for running two replicas of an Nginx container labeled as `app: myapp`.
- [service.yaml](c:\Users\prata\OneDrive\Desktop\t5\service.yaml): Defines a NodePort Service to expose the Nginx deployment on port 80.

## Usage

1. Apply the deployment:
   ```sh
   kubectl apply -f deployment.yaml
   ```

2. Apply the service:
   ```sh
   kubectl apply -f service.yaml
   ```

3. Find the NodePort assigned:
   ```sh
   kubectl get service myapp-service
   ```

4. Access Nginx via `<NodeIP>:<NodePort>` in your browser.

## Notes

- The deployment uses the latest Nginx image.
- The service exposes the deployment using a NodePort for external access.