# Implementing a Public Load Balancer

In Azure, administrators use public load balancers to efficiently manage incoming internet traffic. Public load balancers map public IP addresses and port numbers to the private IP addresses and port numbers of virtual machines. This mapping also extends to response traffic from the virtual machines.

## Load-Balancing Rules for Efficient Traffic Distribution

Load-balancing rules play a crucial role in determining how specific types of traffic are distributed across multiple virtual machines or services. Let's consider a common business scenario to understand how this works:

### Business Scenario

Imagine a scenario where internet traffic needs to reach virtual machines in a web tier subnet. To achieve this, a public load balancer is implemented. Here's how it works:

1. **Internet Traffic**: Internet clients send webpage requests to the public IP address of a web app on TCP port 80.

2. **Azure Load Balancer**: Azure Load Balancer intercepts the incoming traffic.

3. **Traffic Distribution**: The load balancer uses predefined load-balancing rules to distribute these requests across the virtual machines in the load-balanced set.

This setup ensures that incoming web requests from the internet are efficiently distributed among multiple web servers, optimizing the performance and availability of your application.

Implementing a public load balancer simplifies the process of managing incoming internet traffic and ensures that your services remain highly available and responsive.
