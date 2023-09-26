# Creating Health Probes

Health probes are essential for monitoring the status of your application and enabling your load balancer to dynamically manage virtual machines based on their response to health checks. When a probe detects an unhealthy virtual machine, the load balancer stops sending new connections to that instance.

## Things to Know about Health Probes

Here are key points to understand about health probes:

- **Probe Types**: You can configure custom health probes in two main ways: HTTP and TCP.

- **HTTP Probes**: In an HTTP probe, the load balancer checks your back-end pool endpoints every 15 seconds. A virtual machine instance is considered healthy if it responds with an HTTP 200 message within the specified timeout period (default is 31 seconds). Any status other than HTTP 200 is considered unhealthy.

- **TCP Probes**: TCP probes establish a successful TCP session to a defined probe port. If the specified listener on the virtual machine exists, the probe succeeds. If the connection is refused, the probe fails.

- **Probe Configuration**: When configuring a probe, you specify the following settings:
  - Port: The back-end port.
  - URI: The URI for requesting the health status from the backend.
  - Interval: The time between probe attempts (default is 15 seconds).
  - Unhealthy Threshold: The number of failures required for an instance to be considered unhealthy.

- **Guest Agent Probe**: There's also a third option, known as the Guest agent probe, which uses the guest agent inside the virtual machine. However, this option is not recommended when an HTTP or TCP custom probe configuration is possible.

Properly configuring health probes is crucial for ensuring the reliability and availability of your application through the load balancer.
