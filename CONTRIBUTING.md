# Contributing

## Template development and testing

### Local testing

To test the template without actually deploying it there are two basic tools that you can use

1. The [Azure Resource Manager Template Toolkit](https://github.com/Azure/arm-ttk) provides a series of scripts for enforcing best practices when writing templates.
   These are best practices and we do not follow all of them. In particular, currently we do not follow the rules for API versions and `concat` usage.
   It is recommended that you compare the output of the script for the template you are modifying before and after your changes to check that you do not introduce any new issues.
2. You can run some checks if you follow the Usage instructions but append the `-WhatIf` command to do a dry run.

### Testing deployment

You can deploy the template following the usage instructions on the README.
After deployment, it can  be useful to log into a node to debug it.

To do that you need to connect via the load balancer, which is assigned a public IP and handles automatically the assignment of a port for each node.
You can find the IP-port combination to log into a specific node by looking at the "inbound NAT rules" on the Azure portal.
