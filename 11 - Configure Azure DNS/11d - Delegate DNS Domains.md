# Delegate DNS Domains

Delegating your domain to Azure DNS involves identifying the DNS name servers for your DNS zone. Azure DNS automatically allocates DNS name servers from a pool when a DNS zone is created. These name servers are used to create authoritative NS (Name Server) records in your DNS zone.

The delegation process for your domain includes several steps:

1. **Identify Your DNS Name Servers:** You need to find out the DNS name servers assigned to your DNS zone. You can easily do this through the Azure portal. For example, Azure might assign name servers like `ns1-02.azure-dns.com`, `ns2-02.azure-dns.net`, `ns3-02.azure-dns.org`, and `ns4-02.azure-dns.info` to your DNS zone.

2. **Update Your Parent Domain:** Once you can identify your DNS name servers, you must update your parent domain. This step involves working with your registrar, the third-party domain registrar where you registered your domain.

   Here's a basic process to update your parent domain information with your registrar:
   - Access your registrar's DNS management page.
   - Locate the existing NS records for your parent domain.
   - Replace the existing NS records with the NS records created for your domain by Azure DNS.

   Keep in mind that when you copy an NS record (a DNS name server address), be sure to include the trailing period (.) at the end of the address. This period indicates the end of a fully qualified domain name.

   It's also important to use the exact names of the DNS name servers as created by Azure DNS. We recommend copying all DNS name server NS records for your domain to the parent domain, regardless of whether you expect traffic on them.

3. **Delegate Subdomains (Optional):** If you need to delegate a subdomain for your domain, you can do so by setting up a separate child DNS zone. This process is similar to the delegation of the parent domain, but it's managed within the Azure portal.

   To delegate a subdomain, follow these steps:
   - Go to the parent DNS zone for your domain in the Azure portal.
   - Find the existing NS records for your parent domain.
   - Create new NS records for your child DNS zone (subdomain).

   Note that the parent and child DNS zones can be in the same or different resource groups. The NS record server name in the child DNS zone typically includes the subdomain name, such as `partners.azureadmininc.org`.

These steps help you effectively delegate your DNS domains and subdomains using Azure DNS.
