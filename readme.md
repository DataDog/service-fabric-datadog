# Datadog Service Fabric Cluster Template

These ARM templates set up an insecure Service Fabric cluster that includes the Datadog Agent on each node as a VM extension.

## Usage

There are two templates: one that sets up a Windows cluster and another one that sets up a Linux cluster.
First, select the template you want to use and fill in the parameters, including Datadog's API key, Datadog's site and the administrator password for each node's administrator account.

After that, use the [Azure PowerShell module](https://docs.microsoft.com/en-us/powershell/azure/install-az-ps) to 

1. [create a resource group](https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup) and 
2. [deploy this repository's template](https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment).

Assuming the relevant variables are set an example command sequence for the deployment could be:

``` powershell
Login-AzAccount
New-AzResourceGroup -Name $ResourceGroup -Location "eastus"
New-AzResourceGroupDeployment -ResourceGroupName $ResourceGroup -TemplateFile $TemplateFile -TemplateParameterFile $ParametersFile -Verbose
```
