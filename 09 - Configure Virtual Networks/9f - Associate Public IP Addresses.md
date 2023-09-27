# Associate Public IP Addresses

In Azure, you can associate a public IP address resource with various types of Azure resources to enable communication between these resources and the internet. Public IP addresses can be associated with virtual machine network interfaces, internet-facing load balancers, VPN gateways, and application gateways. It's worth noting that you can associate both dynamic and static public IP addresses with these resources.

## Things to Consider

When associating public IP addresses, you should consider the following:

### Resource Type

The type of Azure resource you want to associate a public IP address with determines how you perform the association. Here's a summary:

- **Virtual Machine**: You can associate a public IP address with the network interface card (NIC) of a virtual machine. This allows the virtual machine to communicate with the internet. Both dynamic and static IP addresses can be used.

- **Load Balancer**: For internet-facing load balancers, you configure the association in the front-end configuration. Like virtual machines, both dynamic and static IP addresses are supported.

- **VPN Gateway**: Public IP addresses can be associated with the VPN gateway's IP configuration. Both dynamic and static IP addresses are possible, but static IP addresses might have restrictions based on SKUs.

- **Application Gateway**: In the case of application gateways, you associate the public IP address in the front-end configuration. Just like other resources, both dynamic and static IP addresses can be used. However, static IP addresses might have SKU-specific limitations.

### Public IP Address SKUs

When creating a public IP address, you have the option to choose between the Basic and Standard SKUs. This choice impacts various aspects of the IP address, including assignment method, security, available resources, and redundancy options. Here's a quick comparison:

#### Basic SKU:

- **IP Assignment**: Supports both static and dynamic IP addresses.
- **Security**: Open by default, which means it allows inbound traffic.
- **Resources**: Compatible with network interfaces, VPN gateways, application gateways, and internet-facing load balancers.
- **Redundancy**: Not zone redundant.

#### Standard SKU:

- **IP Assignment**: Supports only static IP addresses.
- **Security**: Secure by default, which means it's closed to inbound traffic and you must configure rules to allow traffic.
- **Resources**: Compatible with network interfaces and public standard load balancers.
- **Redundancy**: Zone redundant by default.

Understanding the differences between these SKUs is essential for making the right choice when creating and associating public IP addresses with your Azure resources. Your selection should align with your specific requirements for IP assignment, security, resource compatibility, and redundancy.
