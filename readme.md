# Service Fabric Cluster with Datadog installed as a VM extension on each node

These ARM templates set up unsecure Service Fabric clusters that include the Datadog agent on each node as a VM extension.

## PowerShell commands to run:

```powershell
Login-AzureRmAccount

Select-AzureRmSubscription -SubscriptionId <SubscriptionId>

$ResouceGroup = <resourceGroupName>

New-AzureRmResourceGroup -Name $ResouceGroup -Location "eastus"

New-AzureRmResourceGroupDeployment -ResourceGroupName $ResouceGroup -TemplateFile '<Path to template_datadog.json>' -TemplateParameterFile '<Path to parameters.json>' -Verbose
```