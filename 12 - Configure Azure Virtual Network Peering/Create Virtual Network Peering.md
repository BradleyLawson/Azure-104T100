# Creating Virtual Network Peering 

Azure Virtual Network peering can be set up for virtual networks using various methods, including PowerShell, Azure CLI, and the Azure portal. In this guide, we focus on creating peering in the Azure portal for virtual networks deployed through Azure Resource Manager.

## What You Need to Know

Before creating virtual network peering, consider the following:

- Your Azure account must have the Network Contributor or Classic Network Contributor role, or a custom role with the required permissions.
- You need two virtual networks to create a peering.
- Initially, virtual machines in these networks can't communicate. After peering, they can based on your configuration.

## How to Create Virtual Network Peering

1. Sign in to the Azure portal and select the appropriate subscription.

2. Create two virtual networks. At least one must be deployed using Azure Resource Manager.

3. Choose the first virtual network for peering, go to Settings, and click Add Peering.

4. Configure the peering settings:
   - Give the peering a unique name.
   - Choose how traffic to the remote network is managed (Allow or Block).
   - Specify how traffic from the remote network is handled (Allow or Block).
   - Decide whether to use an Azure VPN gateway.

5. Configure peering parameters for your remote virtual network in the same dialog.

6. Create at least one virtual machine in each virtual network.

7. Test communication between the virtual machines within the peered network.

## Checking Peering Status

In the Azure portal, you can check the status of your virtual network peering. Successful peering is confirmed when both virtual networks show a status of "Connected."

For Azure Resource Manager deployments, look for "Initiated" and "Connected" status conditions. For classic deployments, you'll also see an "Updating" status condition.

When you initiate the first peering from one virtual network to another, the status of the first virtual network is "Initiated." When you complete the peering from both networks, both virtual networks show a "Connected" status.
