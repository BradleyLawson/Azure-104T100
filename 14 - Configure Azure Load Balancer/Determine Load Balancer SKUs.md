# Determining Azure Load Balancer SKUs 

When setting up an Azure load balancer in the Azure portal, you have to make a crucial choice regarding the type of load balancer (internal or public) and the SKU to use. Azure Load Balancer offers three SKU options: Basic, Standard, and Gateway. Each SKU offers different features, scalability options, and pricing considerations.

## Things to Know about Azure Load Balancer SKUs

Let's explore some essential points to keep in mind when selecting the right SKU for your load balancer:

- **Standard Load Balancer**: This is the latest product and effectively encompasses all the features of the Basic Load Balancer.

- **Standard SKU Features**: The Standard SKU provides an extensive and more detailed set of features compared to the Basic SKU.

- **Upgrading**: While the Basic SKU can be upgraded to the Standard SKU, it's advisable for new designs and architectures to opt for the Standard SKU from the start.

- **Gateway SKU**: The Gateway SKU is designed for high-performance and high-availability scenarios, particularly when using third-party network virtual appliances (NVAs).

## Feature Comparison: Basic vs. Standard SKU

Let's compare how some key features are implemented in the Basic and Standard SKUs:

| Feature           | Basic SKU                    | Standard SKU                |
|-------------------|------------------------------|-----------------------------|
| Health Probes     | HTTP, TCP                    | HTTPS, HTTP, TCP            |
| Availability Zones| Not available                | Zone-redundant and zonal frontends |
| Multiple Frontends| Inbound only                | Inbound and outbound        |
| Security          | - Open by default            | - Closed to inbound flows unless allowed by NSGs |
|                   | - (Optional) Control through | - Internal traffic from the virtual network to the internal load balancer is allowed |

Choosing the appropriate SKU depends on your specific requirements, including features needed, scalability, and the complexity of your architecture. Keep these factors in mind when configuring your Azure Load Balancer.
