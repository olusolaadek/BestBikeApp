## Publish

cd ~/BestBikeApp
dotnet publish -o pub
cd pub
zip -r site.zip \*

## Deployment to Azure

az webapp deployment source config-zip \
 --src site.zip \
 --resource-group learn-34008ec5-a18d-40b7-8c11-ab076d6d54df \
 --name <your-app-name>

## Delete Azure resource group

az group delete --name webappdata --no-wait --yes
