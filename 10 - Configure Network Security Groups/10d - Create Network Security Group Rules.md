# Create Network Security Group Rules

In Azure, Network Security Groups (NSGs) are a powerful way to control inbound and outbound network traffic for your virtual machines. You can easily configure security rules to manage access to various communication services such as HTTPS, RDP, FTP, and DNS.

## Configuring Security Rules

To create effective security rules, you need to specify various properties. Here are some key settings to consider when configuring your security rules:

- **Source**: This identifies how the security rule controls inbound traffic. You can specify a source IP address range that's allowed or denied. The source filter can include any resource, an IP address range, an application security group, or a default tag.

- **Destination**: This identifies how the security rule controls outbound traffic. Similar to the source, you specify a destination IP address range that's allowed or denied. The destination filter can include any resource, an IP address range, an application security group, or a default tag.

- **Service**: You specify the destination protocol and port range for the security rule. You can choose from predefined services like RDP or SSH or provide a custom port range. Azure offers a wide range of services to select from.

- **Priority**: Each security rule is assigned a priority order value. Rules are processed based on the priority order across all rules for a network security group, including those for subnets and network interfaces. The lower the priority value, the higher the precedence of the rule.

When configuring your security rules, consider the specific traffic rules you need to create to meet your network requirements. Azure provides a user-friendly interface in the portal to help you define these rules effectively.
