# azure bastion lab

This creates a resource group, a hub vnet with a standard sku Azure Bastion and a spoke vnet peered to the hub vnet. Also creates Windows VM's with no public ip's are created to access via bastion. The bastion host is set to allow shareable links, ip connectivity and native client support. This also creates a logic app that will delete the resource group in 24hrs. You'll be prompted for the resource group name, location where you want the resources created, your public ip and username and password to use for the VM's. 

More info on Bastion connectivity:
https://learn.microsoft.com/en-us/azure/bastion/connect-vm-native-client-windows,

https://learn.microsoft.com/en-us/azure/bastion/connect-ip-address,

https://learn.microsoft.com/en-us/azure/bastion/shareable-link

The topology will look like this:
![azbastionlab](https://github.com/quiveringbacon/azurebastionlab/assets/128983862/9a0c9fba-0a6f-49f6-90de-0f0591012f0c)

You can run Terraform right from the Azure cloud shell by cloning this git repository with "git clone https://github.com/quiveringbacon/azurebastionlab.git ./terraform".

Then, "cd terraform" then, "terraform init" and finally "terraform apply -auto-approve" to deploy.
