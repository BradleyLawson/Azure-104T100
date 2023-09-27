# Subnets 

Subnets are like virtual compartments within your network. They help organize and secure your network.

## What You Need to Know

- Each subnet has a range of IP addresses.
- A subnet's IP range must be unique in your network.
- Subnet IP ranges can't overlap.
- IP ranges are specified using CIDR notation.

You can create subnets in the Azure portal.

## Reserved Addresses

Azure reserves five IP addresses for each subnet:

1. `192.168.1.0`: Identifies the virtual network address.
2. `192.168.1.1`: Azure's default gateway address.
3. `192.168.1.2` and `192.168.1.3`: Azure DNS IPs for the virtual network.
4. `192.168.1.255`: The virtual network's broadcast address.

## Things to Consider

When planning subnets in your virtual network, keep these scenarios in mind:

1. **Service Requirements**: Some services need their own subnet, so plan for that. Also, ensure enough free IP space. For example, if you connect to an on-premises network via Azure VPN Gateway, allocate a subnet for it.

2. **Network Virtual Appliances**: By default, Azure routes traffic between all subnets. You can change this to route traffic through a network virtual appliance. Useful if you want traffic between subnets to pass through it.

3. **Service Endpoints**: You can limit access to Azure resources (like storage or databases) to specific subnets using service endpoints. You can also block internet access. Customize subnets accordingly.

4. **Network Security Groups**: Each subnet can have a network security group. These groups control traffic to and from subnets. You can have different rules for different subnets.

5. **Private Links**: Azure Private Link provides secure, private connections from your virtual network to Azure services. It's a way to keep data off the public internet.

That's the lowdown on subnets!
