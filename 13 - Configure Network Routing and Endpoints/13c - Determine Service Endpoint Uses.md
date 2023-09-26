# Determining Service Endpoint Uses

A virtual network service endpoint serves as a way to identify your virtual network to Azure services. Once service endpoints are enabled in your virtual network, you can secure Azure service resources by adding virtual network rules to these resources.

## Key Points about Service Endpoints

Let's explore the essential characteristics of service endpoints:

- Service endpoints allow you to extend your virtual network's identity to Azure services, enhancing the security of your service resources.

- Azure service resources can be secured to your virtual network by creating virtual network rules.

- Virtual network rules have the power to remove public internet access to resources, permitting traffic solely from your virtual network.

- Service endpoints ensure that service traffic flows directly from your virtual network to Azure services via the Microsoft Azure backbone network.

- Configuration of service endpoints is done through the subnet, making it an efficient and hassle-free process.

## Business Scenario

Consider a scenario where a virtual machine within a subnet needs to access an Azure Storage account through a service endpoint. Virtual network rules enable this access while blocking communication with the public internet. The diagram below illustrates this situation:

[Diagram not included]

## Advantages of Using Service Endpoints

Using service endpoints can offer several advantages:

- Enhanced Security: Implement service endpoints to bolster the security of your Azure service resources. They remove public internet access and allow traffic exclusively from your virtual network.

- Optimal Routing: In some cases, routing in your virtual network may inadvertently force Azure service traffic to take the same route as internet traffic. Service endpoints provide optimal routing, bypassing such constraints.

- Direct Traffic: Service endpoints keep traffic within the Azure backbone network, facilitating outbound internet traffic auditing and monitoring without affecting service traffic.

- Easy Setup and Maintenance: Configuring service endpoints in your subnets is straightforward and low-maintenance. You no longer need reserved public IP addresses in your virtual networks to secure Azure resources through an IP firewall, and no NAT or gateway devices are required for setting up service endpoints.

**Note**: When using service endpoints, virtual machine IP addresses switch from public to private IPv4 addresses. Existing Azure service firewall rules that rely on Azure public IP addresses may require adjustments. Temporary service traffic interruption may occur during service endpoint configuration.
