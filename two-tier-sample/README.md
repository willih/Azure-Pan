<<<<<<< Updated upstream
# Palo Alto Networks Azure repository

# Support Policy
This ARM template is released under an as-is, best effort, support policy. These scripts should be seen as community supported and Palo Alto Networks will contribute our expertise as and when possible. We do not provide technical support or help in using or troubleshooting the components of the project through our normal support options such as Palo Alto Networks support teams, or ASC (Authorized Support Centers) partners and backline support options. The underlying product used (the VM-Series firewall) by the scripts or templates are still supported, but the support is only for the product functionality and not for help in deploying or using the template or script itself.
Unless explicitly tagged, all projects or work posted in our GitHub repository (at https://github.com/PaloAltoNetworks) or sites other than our official Downloads page on https://support.paloaltonetworks.com are provided under the best effort policy.


# VM-Series with NAT VM, and VM's for Web and DB subnet
=======
# VM-Series with NAT VM, and VM's for Web and DB subnet

This ARM template deploys a VM-Series next generation firewall VM in an Azure resource group alongwith the following resources similar to a typical two tier architecture. It also adds the relevant User-Defined Route (UDR) tables to send all traffic through the VM-Series firewall.

<<<<<<< HEAD
[<img src="http://azuredeploy.net/deploybutton.png"/>](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fnarayan-pan%2Fnarayan-azure-repo/master/test%20drive/azureDeploy.json)

[<img src="https://camo.githubusercontent.com/536ab4f9bc823c2e0ce72fb610aafda57d8c6c12/687474703a2f2f61726d76697a2e696f2f76697375616c697a65627574746f6e2e706e67" data-canonical-src="http://armviz.io/visualizebutton.png" style="max-width:100%;">](https://raw.githubusercontent.com/narayan-pan/narayan-azure-repo/master/test%20drive/azureDeploy.json)


**Virtual Machines:**

- VM-Series Next generation firewall - (D3 VM size)
- NAT VM - an Ubuntu VM (A1) with iptables to forward all packets to Untrust of VM-Series firewall
- Web VM - an Ubuntu VM (A1) that can be setup as a web server
- DB VM - an Ubuntu VM (A1) that can be setup with a database

**Virtual Network (VNET):**

- VNET : 192.168.0.0/16
- Mgmt Subnet: 192.168.0.0/24 - For the firewall's management interface (eth0)
- Untrust Subnet: 192.168.1.0/24 - For eth1 of firewall
- Trust Subnet: 192.168.2.0/24 - For eth2 of firewall
- Web Subnet: 192.168.3.0/24
- DB Subnet: 192.168.4.0/24
- NAT Subnet: 192.168.5.0/24
>>>>>>> Stashed changes

This ARM template deploys a VM-Series next generation firewall VM in an Azure resource group along with a web and db server similar to a typical two tier architecture. It also adds the relevant User-Defined Route (UDR) tables to send all traffic through the VM-Series firewall.


[<img src="http://azuredeploy.net/deploybutton.png"/>](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FPaloAltoNetworks%2Fazure%2Fmaster%2Ftwo-tier-sample%2FazureDeploy.json)

[<img src="https://camo.githubusercontent.com/536ab4f9bc823c2e0ce72fb610aafda57d8c6c12/687474703a2f2f61726d76697a2e696f2f76697375616c697a65627574746f6e2e706e67" data-canonical-src="http://armviz.io/visualizebutton.png" style="max-width:100%;">](https://raw.githubusercontent.com/PaloAltoNetworks/azure/master/two-tier-sample/azureDeploy.json)
