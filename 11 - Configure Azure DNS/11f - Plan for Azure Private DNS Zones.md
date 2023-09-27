# Planning for Azure Private DNS Zones

Azure Private DNS zones allow you to use custom domain names tailored to your organization's needs, enhancing your virtual network architecture. Here's what you need to know about planning for Azure Private DNS:

## Benefits of Azure Private DNS

1. **No Custom DNS Solution Required**: Azure Private DNS eliminates the need for custom DNS solutions that many organizations previously had to create to manage DNS zones within their virtual networks. It leverages Azure's native infrastructure for DNS zone management.

2. **Support for Common DNS Record Types**: Azure Private DNS supports all common DNS record types, including A, AAAA, CNAME, MX, PTR, SOA, SRV, and TXT.

3. **Automatic Hostname Record Management**: Along with hosting custom DNS records, Azure Private DNS automatically maintains hostname records for virtual machines within specified virtual networks. This streamlines domain name management without requiring custom DNS solutions or application modifications.

4. **Hostname Resolution Between Virtual Networks**: Azure Private DNS zones can be shared between virtual networks, enabling simplified cross-network and service-discovery scenarios, such as virtual network peering.

5. **Familiar Tools and User Experience**: Azure Private DNS leverages well-established Azure DNS tools like PowerShell, Azure Resource Manager (ARM) templates, and the REST API, reducing the learning curve.

6. **Split-Horizon DNS Support**: Azure Private DNS supports split-horizon DNS, allowing you to create zones with the same name that resolve to different answers within a virtual network and from the public internet. This is useful for providing dedicated services within your virtual network.

7. **Azure Region Support**: Azure Private DNS zones are available in all Azure regions within the Azure public cloud.


