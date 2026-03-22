# ubuntu-b-net
Ubuntu wuth network tools installed (apt-get install -y iproute2 net-tools iputils-ping dnsutils)

Container image workflow for pushing a local Docker image to Azure Container Registry (ACR) and LATER deploying it to Azure Container Instance (ACI) and Azure Kubernetes Service (AKS).

## Image
- Original local image: `ubuntu_b_net:v2.0`
- ACR login server: `cnk8sstudies-guf7d4fafabxehdy.azurecr.io`
- ACR image path: `cnk8sstudies-guf7d4fafabxehdy.azurecr.io/nwapps/ubuntu_b_net:v2.0`

## Image flow
1. Build or obtain the local image.
2. Tag the image for ACR.
3. Push the image to ACR.
4. *Configure AKS to pull from ACR.
5. *Deploy the image to AKS with Kubernetes manifests.

## Push commands
```bash
docker tag ubuntu_b_net:v2.0 cnk8sstudies-guf7d4fafabxehdy.azurecr.io/nwapps/ubuntu_b_net:v2.0
docker push cnk8sstudies-guf7d4fafabxehdy.azurecr.io/nwapps/ubuntu_b_net:v2.0
