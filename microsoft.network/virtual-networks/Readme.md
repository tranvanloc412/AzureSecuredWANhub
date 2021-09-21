# Sign in to Azure
Connect-AzAccount

$BasePath = "D:\Project\NCS DevNET\Code\AzureSecuredWANhub\microsoft.network\virtual-networks\"
$RGName = "myResourceGroup"

# PowerShell Run Command
New-AzResourceGroupDeployment -ResourceGroupName $RGName -TemplateFile "$BasePath\vnet.json" -TemplateParameterFile "$BasePath\vnet1.parameters.json"