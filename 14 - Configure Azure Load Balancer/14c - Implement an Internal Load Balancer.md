# Implementing an Internal Load Balancer 

Azure administrators use internal load balancers to efficiently direct traffic to resources within a virtual network or resources that use a VPN to access Azure infrastructure. This approach ensures that front-end IP addresses and virtual networks are not directly exposed to the internet, making it suitable for various scenarios.

## Business Scenario

Let's consider a practical business scenario to understand how an internal load balancer works:

### Scenario

Suppose you have an Azure SQL Database tier subnet containing multiple virtual machines, and you implement an internal load balancer. The goal is to distribute incoming database requests to the backend SQL servers. These SQL servers respond on port 1433. Here's how the internal load balancer helps:

1. **Database Requests**: Requests for the database are received by the internal load balancer.

2. **Load-Balancing Rules**: The internal load balancer uses predefined load-balancing rules to determine how to distribute these requests to the backend SQL servers.

This configuration ensures that your SQL servers efficiently handle incoming requests without exposing front-end IP addresses or virtual networks directly to external endpoints.

## Considerations for Using an Internal Load Balancer

You can implement an internal load balancer for various load balancing scenarios, including:

- Load balancing within a virtual network.
- Load balancing from on-premises computers to virtual machines in the same virtual network.
- Managing traffic for multi-tier applications where the back-end tiers are not internet-facing.
- Load balancing for line-of-business applications hosted in Azure, including integration with on-premises servers.

Additionally, you can configure a public load balancer in front of your internal load balancer to create multi-tier applications with enhanced capabilities.

Implementing an internal load balancer simplifies traffic management and enhances the availability of your Azure resources.
