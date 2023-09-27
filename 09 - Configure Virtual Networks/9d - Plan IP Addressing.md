# Plan IP Addressing

In Azure, you can assign IP addresses to resources for communication purposes. There are two primary types of Azure IP addresses: private and public.

## Private IP Addresses

Private IP addresses are used for communication within an Azure virtual network and between your on-premises network and Azure. You typically create a private IP address for your resource when using a VPN gateway or Azure ExpressRoute circuit to extend your network into Azure.

## Public IP Addresses

Public IP addresses allow your resources to communicate with the internet and external services. You can create public IP addresses to connect with Azure's public-facing services and other internet resources.

In the illustration below, you can see a virtual machine resource equipped with both a private IP address and a public IP address:

![Resource with Private and Public IP Addresses](insert_image_link_here)

## Important Points about IP Addresses

Here are some key characteristics of IP addresses in Azure:

- IP addresses can be statically assigned or dynamically assigned based on your requirements.

- Dynamically and statically assigned IP resources can be separated into different subnets.

- Static IP addresses are best suited for specific situations, such as:
  - DNS name resolution, where IP address changes require host record updates.
  - IP address-based security models that demand apps or services to have a static IP.
  - TLS/SSL certificates linked to specific IP addresses.
  - Firewall rules that allow or deny traffic based on IP address ranges.
  - Role-based virtual machines like Domain Controllers and DNS servers.

Planning your IP addressing strategy in Azure is crucial to ensure efficient and secure communication between your resources.

Remember to consider whether you need private or public IP addresses and whether static or dynamic assignment better suits your specific use case.
