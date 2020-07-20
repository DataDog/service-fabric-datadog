# Datadog Service Fabric Cluster Template

These ARM templates set up an insecure Service Fabric cluster that includes the Datadog Agent on each node as a VM extension.

## Usage

Use the [Azure PowerShell module](https://docs.microsoft.com/en-us/powershell/azure/install-az-ps) to 

1. [create a resource group](https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup) and 
2. [deploy this repository's template](https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment).

There are two templates, for both Windows and Linux.
