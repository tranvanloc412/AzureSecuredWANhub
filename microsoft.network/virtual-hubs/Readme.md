# Sign in to Azure
Connect-AzAccount

$BasePath = "D:\Project\NCS DevNET\Code\AzureSecuredWANhub\microsoft.network\virtual-hubs\" <br />
$RGName = "myResourceGroup"

# PowerShell Run Command
New-AzResourceGroupDeployment -ResourceGroupName $RGName -TemplateFile "$BasePath\virtual-hub.json" -TemplateParameterFile "$BasePath\virtual-hub.parameters.json"

New-AzResourceGroupDeployment -ResourceGroupName $RGName -TemplateFile "$BasePath\hub-spoke-conn.json" -TemplateParameterFile "$BasePath\hub-spoke01-conn.parameters.json"