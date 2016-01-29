# azure-adfs-template
* Creates ADFS Servers in Azure
* Deploys the following infrastructure:
 * Storage Account
 * Virtual Network
  * Site-to-Site VPN
    * Local Gateway
    * Public IP for Azure Gateway
    * Azure Gateway
    * Gateway Connection
  * 3 subnets: AD, Internal, DMZ
  * 3 Network Security Groups:
    * AD - permits AD traffic, RDP incoming to network; limits DMZ access
    * Internal - permissive; restricts traffic to DMZ
    * DMZ - restrictive; permits 443 traffic to Internal, RDP from internal, very limited traffic from Internal, no traffic to Internet or Internal
  * Public IP Address
  * 2 Load Balancers
    * Internal - to be used to access AD FS Servers
    * External - to be used to access Web Application Proxy servers (via PublicIP)

  _Note: only one VM Size is specified (at this time)_

  _Note: Network Cards and Availability Sets are provisioned for VMs_

  * AD VMs - 2 VMs of size specified
  * AD FS VMs - Number to be specified of size specified
  * WAP VMs - Number to be specified (same as AD FS VMs)


<<<<<<< HEAD
<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fnromyn%2Fazure-adfs-template%2Fmaster%2FTemplates%2FazureDeploy.json" target="_blank">
=======
<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fnromyn%2Fazure-adfs-template%2Fmaster%2FazureDeploy.json" target="_blank">
>>>>>>> 33c2dc400b7e6459edd42bbc6cd8e5aad83581fc
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
