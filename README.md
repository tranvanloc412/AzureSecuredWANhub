# AzureSecuredWANhub

# Sign in to Azure
Connect-AzAccount

<!-- If you have multiple Azure subscriptions, select the subscription you want to use. Replace [SubscriptionID/SubscriptionName] and the square brackets [] with your subscription information: -->
Set-AzContext [SubscriptionID/SubscriptionName]

# Steps:
deploy .\microsoft.resources\resource-groups\resource-groups.json
deploy .\microsoft.network\virtual-networks\vnet.json
deploy .\microsoft.network\virtual-hubs\virtual-hub.json
deploy .\microsoft.network\azure-firewalls\firewall-policy.json
deploy .\microsoft.network\azure-firewalls\azure-firewall.json => **convert vhub to secure hub**.
deploy .\microsoft.network\virtual-hubs\hub-spoke-conn.json => **create hub vnet connection and route table**.