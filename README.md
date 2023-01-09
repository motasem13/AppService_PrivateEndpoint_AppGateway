# Deploying App Service Multi-Tenant, Private Endpoint and internet facing App Gateway

This template deploys an Application Gateway in Azure Virtual Network (subnet), a second subnet that containts a Private endpoint as an App Service interface, an App Service which is configured with a Private endpoint, everything is created with generated names, however, you can easily modify the template to use other default values or parameterize values. You can also 'bring your own' subnet, web app, application gateway or public ip, if you have any of the items already created.




**Note: for production environment it is recommend having a custom domain (and associated certificate) available to avoid having to rely on the default ".azurewebsites" domain, more details: [Configure App Service with Application Gateway](**Note:%20for%20production%20environment%20it%20is%20recommend%20having%20a%20custom%20domain%20%28and%20associated%20certificate%29%20available%20to%20avoid%20having%20to%20rely%20on%20the%20default%20%22.azurewebsites%22%20domain.%20%20more%20details%20%60%5BManage%20traffic%20to%20App%20Service%20-%20Azure%20Application%20Gateway%20%7C%20Microsoft%20Learn%5D%28https://learn.microsoft.com/en-us/azure/application-gateway/configure-web-app?tabs=customdomain,azure-portal%29%60**)`**

To deploy the resource use the following Azure CLI:

```
az group create --name ExampleGroup --location "Central US"

az deployment group create \
  --name ExampleDeployment \
  --resource-group ExampleGroup \
  --template-file <path-to-bicep> \
```



`Tags: appService, Microsoft.Network/virtualNetworks, Microsoft.Web/serverfarms, Microsoft.Web/sites, Microsoft.Web/sites/config, Microsoft.Web/sites/hostNameBindings, Microsoft.Web/sites/networkConfig, Microsoft.Network/privateEndpoints, Microsoft.Network/privateDnsZones, Microsoft.Network/privateDnsZones/virtualNetworkLinks, Microsoft.Network/privateEndpoints/privateDnsZoneGroups`