# Allocate or Assign Private IP Addresses

In Azure, you can allocate or assign private IP addresses to various resources like virtual machine network interfaces, internal load balancers, and application gateways. These private IP addresses are essential for internal communication within Azure.

## Things to Consider

When working with private IP addresses, consider the following:

### Resource Type

The type of Azure resource you want to associate a private IP address with determines how you perform the association. Here's a summary:

- **Virtual Machine**: You can associate a private IP address with the network interface card (NIC) of a virtual machine. Both dynamic and static IP addresses are supported.

- **Internal Load Balancer**: For internal load balancers, you configure the association in the front-end configuration. Both dynamic and static IP addresses are supported.

- **Application Gateway**: When dealing with application gateways, you associate the private IP address in the front-end configuration. Just like other resources, both dynamic and static IP addresses can be used.

### Private IP Address Assignment

Private IP addresses can be assigned in two ways: dynamic and static.

#### Dynamic:

- Azure automatically assigns the next available unassigned or unreserved IP address within the subnet's address range.
- This is the default allocation method.
- For example, if addresses 10.0.0.4 through 10.0.0.9 are already assigned to other resources, Azure assigns the next available address, such as 10.0.0.10, to a new resource.

#### Static:

- You have the flexibility to select and assign any unassigned or unreserved IP address within the subnet's address range.
- Useful when you require specific IP addresses for your resources.
- For instance, if a subnet's address range is 10.0.0.0/16, and addresses 10.0.0.4 through 10.0.0.9 are already assigned, you can manually assign an address between 10.0.0.10 and 10.0.255.254.

Understanding these options for private IP address allocation and assignment helps you tailor your Azure resources to your specific networking needs.
