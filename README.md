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
5. screenshots
<img width="1577" height="620" alt="Screenshot 2025-09-29 231937" src="https://github.com/user-attachments/assets/ef24a7c9-49d0-41dd-babc-a44a1f07b913" />
<img width="1577" height="654" alt="Screenshot 2025-09-29 233538" src="https://github.com/user-attachments/assets/d713edc9-b1d4-4b27-9ac4-12db3023c70a" />
<img width="1584" height="668" alt="Screenshot 2025-09-29 233627" src="https://github.com/user-attachments/assets/79f38ade-22db-4cf0-a121-1b89d3d7e279" />
<img width="1547" height="702" alt="Screenshot 2025-09-29 234936" src="https://github.com/user-attachments/assets/de9d83c8-7b2b-4190-92c7-e71dbdb6e489" />
<img width="1532" height="996" alt="Screenshot 2025-09-29 234957" src="https://github.com/user-attachments/assets/ab1b1c69-f27e-456f-b9a2-b1ea8bf52a45" />
<img width="1549" height="976" alt="Screenshot 2025-09-29 235015" src="https://github.com/user-attachments/assets/e553590c-ecd3-455e-8b60-ce6be27f0be2" />

## Notes

- The deployment uses the latest Nginx image.
- The service exposes the deployment using a NodePort for external access.
