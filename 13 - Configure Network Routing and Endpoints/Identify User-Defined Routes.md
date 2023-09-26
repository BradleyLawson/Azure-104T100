# Identifying User-Defined Routes

While Azure automatically handles network traffic routing, there are situations where custom configurations are preferred. This is where User-Defined Routes (UDRs) and Next Hop targets come into play.

## Key Points about User-Defined Routes

Let's explore the key characteristics of User-Defined Routes:

- UDRs control network traffic by specifying routes that define the next hop for that traffic.

- The next hop can be one of the following targets:
  - Virtual network gateway
  - Virtual network
  - Internet
  - Network Virtual Appliance (NVA)

- Similar to system routes, UDRs also interact with route tables.

- Each route table can be associated with multiple subnets.

- However, each subnet can be associated with only one route table.

- Importantly, there are no charges for creating route tables in Microsoft Azure.

## Business Scenario

Imagine you have a virtual machine performing network functions like routing, firewalling, or WAN optimization. You need to direct specific subnet traffic to a Network Virtual Appliance (NVA). To achieve this setup, you can place the NVA between subnets or between a subnet and the internet. Subnets can use UDRs to access the NVA and then connect to the internet. Additionally, another UDR and NVA can be used to access the back-end subnet. 
