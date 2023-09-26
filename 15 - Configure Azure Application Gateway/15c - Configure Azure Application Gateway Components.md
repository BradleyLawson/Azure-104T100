# Configure Azure Application Gateway Components

**Objective:** Azure Application Gateway comprises several components that collaborate to route requests to a pool of web servers and monitor their health. These components include the front-end IP address, back-end pools, routing rules, health probes, and listeners. Additionally, there's an option to implement a firewall for added security.

## Key Points

### How Application Gateway Components Work Together

Let's explore how these components of an Application Gateway function together:

1. **Front-end IP Address:** This is where client requests are received. Your Application Gateway can have a public or private IP address, or both, but only one of each.

2. **Optional Firewall:** Incoming traffic is checked for common threats before reaching the listeners, providing an additional layer of security.

3. **Listeners:** One or more listeners receive incoming traffic and route requests to the appropriate back-end pool based on specified criteria. Listeners can be either Basic or Multi-site, depending on routing requirements. They also handle TLS/SSL certificates for secure communication.

4. **Routing Rules:** Routing rules define how to analyze requests and direct them to the suitable back-end pool. These rules consider elements like hostname, path, and protocol. Associated HTTP settings determine how traffic is encrypted between Application Gateway and back-end servers, along with other configuration details.

5. **Back-end Pools:** Back-end pools group web servers, including virtual machines, Virtual Machine Scale Sets, Azure App Services, or on-premises servers. Each pool has its own load balancer for distributing work across the servers.

6. **Health Probes:** Health probes assess the availability of servers in your back-end pool. Application Gateway uses health probes to send requests to servers and considers them healthy if they return an HTTP response with a status code between 200 and 399. If you don't configure a health probe, Application Gateway creates a default one that waits for 30 seconds before marking a server as unhealthy.

7. **Optional Firewall (if enabled):** You can enable Azure Web Application Firewall to inspect incoming requests for threats based on OWASP rules. This firewall enhances security by protecting against threats like SQL injection, cross-site scripting, and more. It supports rule sets like CRS 2.2.9 and CRS 3.0.

These components collaborate to ensure effective routing, load balancing, and security within your Azure Application Gateway configuration.
