# Deploying Code from GitHub to Azure App Service
This file contains URLs from the demos in Cloud Academy's _Deploying Code from GitHub to Azure App Service_ course.  

### Create a resource group
```
az group create --name webapprg --location westus
```

### Create an App Service Plan
```
az appservice plan create --name asplan --resource-group webapprg --location westus --sku F1
```

### Create a webapp
```
az webapp create --name <app_name> --resource-group webapprg --plan asplan
```

### Deploy an app from GitHub to Azure App Service
```
az webapp deployment source config --repo-url https://github.com/Azure-Samples/html-docs-hello-world --branch master --manual-integration --name <app_name> --resource-group webapprg
```

### URL of webapp
https://<app_name>.azurewebsites.net
