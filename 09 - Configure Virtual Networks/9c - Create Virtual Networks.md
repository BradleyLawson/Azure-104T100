# Creating Virtual Networks

Creating virtual networks in Azure is a straightforward process, but there are some essential points to keep in mind:

## Address Space

- Define the IP address space for your virtual network.
- Ensure it doesn't overlap with existing IP spaces in your organization.
- Choose between on-premises or cloud address space; you can't mix both.
- Once created, you can't change the address space.

## Subnets

- Each virtual network must have at least one subnet.
- Subnets have their IP address range within the virtual network space.
- Subnet address ranges must be unique within the virtual network.
- They cannot overlap with other subnet ranges in the same virtual network.

## How to Create

You can easily create a virtual network in the Azure portal. Just provide:

- Azure subscription
- Resource group
- Virtual network name
- Service region for the network

**Note:** Keep in mind that default limits on Azure networking resources may change, so always refer to the latest Azure networking documentation for up-to-date information.
