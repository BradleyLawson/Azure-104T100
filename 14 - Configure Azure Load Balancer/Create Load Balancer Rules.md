# Creating Load Balancer Rules

Load-balancing rules play a crucial role in specifying how traffic is distributed among your back-end pools. Each rule associates a front-end IP address and port combination with a set of back-end IP address and port combinations.

## Things to Know about Load-Balancing Rules

Here's what you need to understand about configuring load-balancing rules for your back-end pools:

- **Rule Components**: To create a load-balancing rule, you must have a frontend, backend, and health probe configured for your load balancer.

- **Rule Configuration**: When defining a rule in the Azure portal, you'll configure several settings, including:
  - IP version (IPv4 or IPv6)
  - Front-end IP address, port, and protocol (TCP or UDP)
  - Back-end pool and back-end port
  - Health probe
  - Session persistence

- **Load Distribution**: By default, Azure Load Balancer evenly distributes network traffic across multiple virtual machines. It uses a five-tuple hash, considering source IP address, source port, destination IP address, destination port, and protocol type. Session persistence within a transport session is provided.

- **Session Persistence**: Session persistence determines how traffic from a client is handled. Options include:
  - None (default): Any virtual machine can handle the request.
  - Client IP: Successive requests from the same client IP address are handled by the same virtual machine.
  - Client IP and protocol: Successive requests from the same client IP address and protocol combination are handled by the same virtual machine.

- **Combining Rules**: Load-balancing rules can be used in conjunction with NAT rules. For example, you can use NAT to allow remote desktop access from outside Azure by combining NAT rules with load-balancing rules.

Load-balancing rules are essential for optimizing the distribution of traffic to your back-end resources and ensuring the efficient operation of your load balancer.
