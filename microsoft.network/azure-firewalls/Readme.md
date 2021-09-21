# Sign in to Azure
Connect-AzAccount

$BasePath = "D:\Project\NCS DevNET\Code\AzureSecuredWANhub\microsoft.network\azure-firewalls\" <br />
$RGName = "myResourceGroup"

# PowerShell Run Command
New-AzResourceGroupDeployment -ResourceGroupName $RGName -TemplateFile "$BasePath\firewall-policy.json" -TemplateParameterFile "$BasePath\firewall-policy.parameters.json"

New-AzResourceGroupDeployment -ResourceGroupName $RGName -TemplateFile "$BasePath\azure-firewall.json" -TemplateParameterFile "$BasePath\azure-firewall.parameters.json"