# Sign in to Azure
Connect-AzAccount

$BasePath = "D:\Project\NCS DevNET\Code\AzureSecuredWANhub\microsoft.resources\resource-groups\"

# PowerShell Run Command
New-AzSubscriptionDeployment -Location "Southeast Asia" -TemplateFile "$BasePath\resource-groups.json"
