# Implement Network Security Groups

In Azure, you have the capability to control and restrict network traffic to your resources within a virtual network by utilizing Network Security Groups (NSGs). NSGs allow you to define security rules that govern inbound and outbound network traffic.

## Key Characteristics of Network Security Groups

Here are some important aspects to understand about Network Security Groups:

- **Security Rules**: NSGs are composed of a list of security rules that dictate whether to allow or deny network traffic, both incoming and outgoing.

- **Associations**: NSGs can be associated with either subnets or network interfaces, depending on your specific needs.

- **Multiple Associations**: It's possible to associate a single NSG multiple times for different use cases.

- **Configuration**: You can create and configure NSGs directly in the Azure portal.

## Working with Network Security Groups

When dealing with virtual machines and NSGs, you can view and manage network security groups through the Azure portal. For each virtual machine, you can access an Overview page that provides details about the associated network security groups, including information about assigned subnets, network interfaces, and defined security rules.

## NSGs and Subnets

One key use case for NSGs is to assign them to subnets, creating what's commonly referred to as a "protected screened subnet" or DMZ (Demilitarized Zone). A DMZ serves as a buffer zone between resources within your virtual network and the internet. It allows you to restrict traffic flow to all machines residing within the subnet.

Keep in mind:

- Each subnet can have at most one associated network security group.

## NSGs and Network Interfaces

Network Security Groups can also be assigned to network interface cards (NICs). This enables you to define rules that control all traffic passing through a specific NIC. In a subnet, each network interface can have either zero or one associated network security group.

By leveraging Network Security Groups, you can enforce security policies and access controls effectively within your Azure virtual network, enhancing the overall security posture of your resources.
