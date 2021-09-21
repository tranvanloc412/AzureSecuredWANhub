# Sign in to Azure
Connect-AzAccount

$BasePath = "D:\Project\NCS DevNET\Code\AzureSecuredWANhub\microsoft.resources\resource-groups\"
$RGName = "myResourceGroup"

# PowerShell Run Command
New-AzResourceGroupDeployment -ResourceGroupName $RGName -TemplateFile "$BasePath\vnet.json"