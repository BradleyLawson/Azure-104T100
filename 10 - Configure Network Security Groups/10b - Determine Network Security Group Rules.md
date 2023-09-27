# Determine Network Security Group Rules

In Azure, Network Security Groups (NSGs) allow you to set up rules that control and filter network traffic for both inbound and outbound communications. Understanding these rules is crucial for managing the security of your resources within a virtual network.

## Key Characteristics of Security Rules in NSGs

Let's delve into the essential aspects of security rules in Network Security Groups:

- **Default Rules**: When you create an NSG, Azure automatically generates default security rules, both for inbound and outbound traffic. Examples of default rules include "DenyAllInbound" (denies all incoming traffic by default) and "AllowInternetOutbound" (allows outbound traffic to the internet).

- **Custom Rules**: You can extend the security rules by adding your own custom rules based on specific conditions. These conditions include settings like:
  - Name
  - Priority
  - Port
  - Protocol (Any, TCP, UDP)
  - Source (Any, IP addresses, Service tag)
  - Destination (Any, IP addresses, Virtual network)
  - Action (Allow or Deny)

- **Priority**: Each security rule is assigned a Priority value. The rules are processed in order of priority, where lower priority values take precedence.

- **Default Rule Override**: While you can't remove the default security rules, you can override them by creating custom rules with higher Priority settings.

## Inbound Traffic Rules

Inbound traffic rules are crucial for defining what traffic is allowed into your resources within a virtual network. Azure sets up three default inbound security rules in every network security group. These default rules essentially deny all incoming traffic except for traffic originating from your virtual network and Azure load balancers.

## Outbound Traffic Rules

Outbound traffic rules control what traffic is allowed to leave your resources. Azure also defines three default outbound security rules for each network security group. These default rules only permit outbound traffic to the internet and within your virtual network.

Understanding and managing these security rules within Network Security Groups is vital for ensuring the security and proper functioning of your Azure resources.
