# Gateway Transit and Connectivity Simplified

When you connect virtual networks through peering, you can set up an Azure VPN Gateway in one of the peered networks to act as a transit point. This allows the peered network to use the remote VPN gateway to access other resources.

## Example Scenario

Imagine three virtual networks in the same region connected through peering. Virtual networks A and B are each peered with a central hub virtual network. This hub network includes various resources, including a gateway subnet and an Azure VPN gateway. The VPN gateway is configured to enable VPN gateway transit. Virtual network B can access hub resources, including the gateway subnet, through this remote VPN gateway.

## Key Points about Azure VPN Gateway

- Each virtual network can have only one VPN gateway.
- Gateway transit works for both regional and global virtual network peering.
- With VPN gateway transit enabled, a virtual network can access resources beyond the peering. For example, it can connect to an on-premises network using site-to-site VPN, establish a vnet-to-vnet connection with another virtual network, or use point-to-site VPN for client connections.
- Gateway transit allows peered networks to share the gateway, eliminating the need to deploy a VPN gateway in each peered network.
- You can control network security group rules when configuring virtual network peering to allow or block access between virtual networks or subnets.