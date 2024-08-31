# Source code

This folder contains files that can be used in this talk if you wish to do it live.

## Demo 3 - Budget Automation 
This demo shows how to configure a budget and trigger an Azure Automation workbook, which changes the firewall settings on the Azure OpenAI resource. In effect, this blocks traffic to the resource, preventing it from hearing any input requests and incurring any more costs. 

AIDenyFirewall.ps - This sets the Azure OpenAI firewall setting to Deny all except for the private endpoints/IP addresses in the Allow list. This is perfect to use if your resource needs to be open to allow all when it's running.

AIRemoveAllowed.ps - This removes any listed IP addresses or ragnes (CIDR) from the Allow list in the Azure OpenAI firewall. This is perfect to use if your resource has already been locked down to only allowed addresses/ranges. For this runbook you will need to specify all of the IP addresses/ranges that you have added to the Allow list. Once removed, this effectively blocks traffic to the resource, preventing it from hearing any input requests and incurring any more costs.


