# AzureSecuredWANhub

# Sign in to Azure
Connect-AzAccount

<!-- If you have multiple Azure subscriptions, select the subscription you want to use. Replace [SubscriptionID/SubscriptionName] and the square brackets [] with your subscription information: -->
Set-AzContext [SubscriptionID/SubscriptionName]

# Deploy RG
New-AzSubscriptionDeployment -Location "Southeast Asia" -TemplateFile .\ResourceGroup.json

# Deploy Vnet
New-AzResourceGroupDeployment -ResourceGroupName <resource-group-name> -TemplateFile <path-to-template>