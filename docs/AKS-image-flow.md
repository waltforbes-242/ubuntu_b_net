## AKS deployment flow
1. Local Docker image `ubuntu_b_net:v2.0` exists on the developer laptop.
2. The image is retagged with the ACR login server and repository path.
3. The tagged image is pushed to ACR.
4. AKS is granted permission to pull from the ACR.
5. Kubernetes deployment manifests reference the ACR image path.
6. AKS pulls the image from ACR and runs the workload.
