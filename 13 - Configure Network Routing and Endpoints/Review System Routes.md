# Reviewing System Routes

In Azure, system routes are essential for directing network traffic among virtual machines, on-premises networks, and the internet. These system routes are organized and managed through route tables.

## Key Points about System Routes

Let's delve into how Azure implements system routes:

- Azure employs system routes to manage traffic in various scenarios, including:
  - Traffic between virtual machines in the same subnet.
  - Traffic between virtual machines in different subnets within the same virtual network.
  - Traffic from virtual machines to the internet.

- Route tables are containers for a set of rules called "routes." These routes define how packets should be routed within a virtual network.

- Each subnet in Azure is associated with a specific route table.

- When a packet leaves a subnet, it's processed based on the associated route table.

- Packets are routed by matching their destination. The destination can be an IP address, a virtual network gateway, a virtual appliance, or the internet.

- If no matching route is found in the route table, the packet is dropped.

## Business Scenario

Consider a virtual network with two subnets. Azure system routes can be used to control communication between these subnets and between subnets and the internet. For instance, a front-end subnet can utilize a system route to access the internet, while a back-end subnet can employ a system route to reach the front-end subnet. Both subnets are connected to a route table. 
