# Thoughtworks

### Overview
Repo with kubernetes helm chart for Mediawiki deployment & Azure DevOps build pipeline model

### Assumptions
While creating this helm chart I have assumed few things which are listed below,
 - Mediawiki application was developed in JAVA
 - Dockerfile to package the code as an image was ready
 - Application code is dockerized & the image was stored in docker registry (ACR)
 - Kubernetes & namespace for the application to be deployed was ready
 - Service connection to connect azure devops with AKS, ACR & github was created

### Tools Used
Tools that are used for Onboarding the application
 - Docker
 - Azure DevOps (CI/CD)
 - Azure Kubernetes Service
 - Azure Container registry
 - Helm

### Guidelines to use the helm chart
 - [Dockerfile](./MediaWiki/dockerfile) : File to create the docker image of the application code
 - [azurepipeline.yaml](./azure-pipelines.yml) : Azure DevOps build pipeline file to dockerize the code
 - [Values.yaml](./MediaWiki/helm/values_dev.yaml) : File that passes the variables to the yamls in helm templates folder. Variables will also be passed through build & release pipeline through Azure DevOps


### Note 
 - Using different values_xxx.yaml files we will be able to customize the deployment for different environments like develop, staging, pre-production & production
