# Review of Azure Private DNS Zone Scenarios

Let's examine some common scenarios for implementing Azure Private DNS zone records.

## Scenario 1: Name Resolution Within a Single Virtual Network

In this scenario, we have a single virtual network containing virtual machines (VMs) that need private name resolution using a specific DNS zone. These DNS records should not be accessible from the internet. Key details:

- Virtual Network 1 includes VMs VM1 and VM2, each with a private IP address.
- An Azure Private DNS zone (e.g., contoso.lab) is linked to Virtual Network 1.
- With Auto registration enabled, Azure DNS automatically creates A records in the DNS zone for VM1 and VM2.
- Azure DNS queries from VM1 in Virtual Network 1 resolve domain names, like VM2.contoso.lab, and return the private IP address of VM2 (e.g., 10.0.0.5).
- Reverse DNS queries (PTR) for private IP addresses work as expected.

## Scenario 2: Name Resolution Across Multiple Virtual Networks

In this scenario, we need name resolution across two virtual networks, a common use case for Azure Private DNS zones. Key details:

- Virtual Network 1 is for registration, and Virtual Network 2 is for name resolution.
- Both networks share a common DNS zone, e.g., contoso.lab.
- Both networks are linked to the common DNS zone.
- Azure Private DNS automatically creates records for VMs in Virtual Network 1.
- Records for VMs in Virtual Network 2 can be created manually.
- Azure DNS resolves domain name queries using both virtual networks.
- Queries from Virtual Network 2 for VMs in Virtual Network 1 return private IP addresses.
- Reverse DNS queries are scoped to the same virtual network, returning the expected results.

These scenarios demonstrate the flexibility and power of Azure Private DNS for custom domain name resolution within and across virtual networks.
