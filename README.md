# custom-nginx
Custom web server based on nginx

Container image workflow for pushing a local Docker image to Azure Container Registry (ACR) and LATER deploying it to Azure Container Instance (ACI) and Azure Kubernetes Service (AKS).

## Image
- Original local image: `custom_nginx:v1.0`
- ACR login server: `cnk8sstudies-guf7d4fafabxehdy.azurecr.io`
- ACR image path: `cnk8sstudies-guf7d4fafabxehdy.azurecr.io/webapps/custom_nginx:v1.0`

## Image flow
1. Build or obtain the local image.
2. Tag the image for ACR.
3. Push the image to ACR.
4. *Configure AKS to pull from ACR.
5. *Deploy the image to AKS with Kubernetes manifests.

## Push commands
```bash
docker tag custom_nginx:v1.0 cnk8sstudies-guf7d4fafabxehdy.azurecr.io/webapps/custom_nginx:v1.0
docker push cnk8sstudies-guf7d4fafabxehdy.azurecr.io/webapps/custom_nginx:v1.0
