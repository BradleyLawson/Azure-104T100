# Determine Network Security Group Effective Rules

In Azure, Network Security Groups (NSGs) play a critical role in controlling network traffic to and from virtual machines. Understanding how these rules are evaluated and applied is essential for managing the security of your virtual network.

## Processing Order for Security Rules

Azure evaluates the defined security rules for each NSG independently. The process differs for inbound and outbound traffic:

- **Inbound Traffic**: Azure first processes the security rules defined at the subnet level, and then it processes rules at the network interface card (NIC) level for any associated virtual machines.

- **Outbound Traffic**: Conversely, for outbound traffic, Azure starts by evaluating rules at the NIC level and then processes subnet-level rules for associated virtual machines.

For both inbound and outbound traffic, Azure also considers how to apply the rules for traffic within the same subnet.

## Effective Security Rules

The effectiveness of your security rules is determined by how Azure applies them within your virtual network. To illustrate this concept, let's consider a virtual network configuration:

[Insert an Illustration or Diagram here to show the network configuration]

In this virtual network, there are three subnets, each containing virtual machines with associated Network Security Groups (NSGs). To control internet traffic over TCP port 80 via the network interface, security rules are needed.

Now, let's evaluate how Azure determines the effective security rules for the virtual machines:

- **VM 1**:
  - Subnet NSG: NSG 1
  - NIC NSG: NSG 2
  - Inbound Rules: NSG 1 subnet rules have precedence over NSG 2 NIC rules
  - Outbound Rules: NSG 2 NIC rules have precedence over NSG 1 subnet rules

- **VM 2**:
  - Subnet NSG: NSG 1
  - NIC NSG: None
  - Inbound Rules: NSG 1 subnet rules apply to both subnet and NIC
  - Outbound Rules: Azure default rules apply to NIC, and NSG 1 subnet rules apply to the subnet only

- **VM 3**:
  - Subnet NSG: None
  - NIC NSG: NSG 2
  - Inbound Rules: Azure default rules apply to the subnet, and NSG 2 rules apply to the NIC
  - Outbound Rules: NSG 2 NIC rules apply to both NIC and subnet

- **VM 4**:
  - Subnet NSG: None
  - NIC NSG: None
  - Inbound Rules: Azure default rules apply to both subnet and NIC, allowing all inbound traffic
  - Outbound Rules: Azure default rules apply to both subnet and NIC, allowing all outbound traffic

Understanding how Azure processes and applies these rules is crucial for effectively managing network security within your virtual network.

