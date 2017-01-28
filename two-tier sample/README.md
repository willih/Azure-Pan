# VM-Series with NAT VM, and VM's for Web and DB subnet

This ARM template deploys a VM-Series next generation firewall VM in an Azure resource group alongwith the following resources similar to a typical two tier architecture. It also adds the relevant User-Defined Route (UDR) tables to send all traffic through the VM-Series firewall.

[<img src="http://azuredeploy.net/deploybutton.png"/>](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FPaloAltoNetworks%2Fnarayan-azure-repo%2Fmaster%2Ftwo-tier%20sample%2FazureDeploy.json)

[<img src="https://camo.githubusercontent.com/536ab4f9bc823c2e0ce72fb610aafda57d8c6c12/687474703a2f2f61726d76697a2e696f2f76697375616c697a65627574746f6e2e706e67" data-canonical-src="http://armviz.io/visualizebutton.png" style="max-width:100%;">](https://raw.githubusercontent.com/PaloAltoNetworks/narayan-azure-repo/master/two-tier%20sample/azureDeploy.json)



**Note:** The template also configures the Azure User-Defined Routing (UDR) table to force all packets through the VM-Series firewall. This provides visibility to all traffic from the VM-Series dashboard and allows you to enforce advanced security policies to protect your Azure deployment.

You can also download the templates and customize them as needed. To deploy them from Azure CLI use the following commands:
```
azure login
azure config mode arm
azure group create -v -n <i>ResourceGroupName</i>  -l <i>AzureLocationName</i>  -d  <i>DeploymentLabel</i>  \
    -f azureDeploy.json  -e azureDeploy.parameters.json
For example:
azure group create  -n myResGp1  -l westus  -d myResGp1Dep1  \
    -f azureDeploy.json  -e azureDeploy.parameters.json
```

#Support Policy
This ARM template is released under an as-is, best effort, support policy. These scripts should be seen as community supported and Palo Alto Networks will contribute our expertise as and when possible. We do not provide technical support or help in using or troubleshooting the components of the project through our normal support options such as Palo Alto Networks support teams, or ASC (Authorized Support Centers) partners and backline support options. The underlying product used (the VM-Series firewall) by the scripts or templates are still supported, but the support is only for the product functionality and not for help in deploying or using the template or script itself.
Unless explicitly tagged, all projects or work posted in our GitHub repository (at https://github.com/PaloAltoNetworks) or sites other than our official Downloads page on https://support.paloaltonetworks.com are provided under the best effort policy.
