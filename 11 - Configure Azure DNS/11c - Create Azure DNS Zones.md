# Create Azure DNS Zones

Azure DNS offers a reliable and secure DNS service for managing and resolving domain names within a virtual network, eliminating the need for custom DNS solutions.

An Azure DNS zone serves as the host for DNS records related to a domain. To start hosting your domain in Azure DNS, you must create a DNS zone for your domain name. All DNS records for your domain will be created inside this DNS zone.

## Things to Know About DNS Zones

You can easily add a DNS zone in the Azure portal, following these steps:

1. Access the Azure portal.

2. Navigate to the DNS settings.

3. Create a DNS zone by specifying the following configuration settings:
   - DNS Zone Name: The name of your DNS zone, which must be unique within the resource group.
   - Number of Records: The number of DNS records you plan to include.
   - Resource Group: The resource group where you want to create the DNS zone.
   - Zone Location: The location for the DNS zone.
   - Associated Subscription: Your Azure subscription.
   - DNS Name Servers: Information about name servers associated with the DNS zone.

By ensuring a unique name for your DNS zone within a resource group, Azure guarantees that the DNS zone doesn't already exist in that specific resource group. However, multiple DNS zones can share the same name, as long as they are in different resource groups or Azure subscriptions. Each instance of a DNS zone with the same name will be assigned to a different DNS name server address.

- The root/parent domain is typically registered at a domain registrar and then pointed to Azure DNS.
- Child domains can be registered directly within Azure DNS.

**Tip:** You don't necessarily need to own a domain name to create a DNS zone with that domain name in Azure DNS. However, domain ownership is required to configure the domain.
