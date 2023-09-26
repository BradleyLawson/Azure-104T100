# Extending Peering with User-Defined Routes and Service Chaining 

Virtual network peering is limited to communication within the peering network. To enable traffic between resources and networks outside this private peering, you need additional mechanisms.

## The Scenario

Imagine you have three virtual networks: A, B, and C. You've set up peering between A and B and also between B and C, but not between A and C. The peering capabilities between B and C don't automatically allow communication between A and C.

## How to Extend Peering

There are several ways to extend your peering capabilities:

- **Hub and Spoke Networks**: Deploy a hub virtual network that can host infrastructure components like a Network Virtual Appliance (NVA) or Azure VPN gateway. All spoke virtual networks can then peer with the hub, allowing traffic to flow through NVAs or VPN gateways in the hub.

- **User-Defined Routes (UDR)**: With virtual network peering, you can set the next hop in a user-defined route to be the IP address of a virtual machine in the peered virtual network or a VPN gateway.

- **Service Chaining**: Service chaining allows you to define user-defined routes that direct traffic from one virtual network to an NVA or VPN gateway.


In summary, these mechanisms let you create a multi-level hub and spoke architecture, overcoming the limit on the number of virtual network peerings per virtual network. User-defined routes and service chaining play a crucial role in extending your peering capabilities.
