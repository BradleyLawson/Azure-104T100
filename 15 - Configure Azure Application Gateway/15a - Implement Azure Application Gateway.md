# Implementing Azure Application Gateway

**Objective:** Administrators use Azure Application Gateway to manage requests from client applications to web apps.

## Business Scenario

Imagine a situation where internet client applications want access to resources in a load-balanced back-end pool. To handle this, we use Azure Application Gateway to listen for HTTP(S) messages and direct them using load-balancing rules to the right resources in the pool.

## Key Points

### Benefits of Azure Application Gateway

- **Application Layer Routing:** Route traffic to web servers based on the URL of a request. Can include Azure virtual machines, Virtual Machine Scale Sets, Azure App Service, or on-premises servers in the back-end pool.

- **Round-Robin Load Balancing:** Distribute incoming traffic evenly across multiple servers. Requests are forwarded in a cycle to balance server load.

- **Session Stickiness:** Ensure that client requests within the same session go to the same back-end server.

- **Supported Protocols:** Supports HTTP, HTTPS, HTTP/2, or WebSocket protocols.

- **Firewall Protection:** Implement a web application firewall to safeguard against web application vulnerabilities.

- **Encryption:** Supports end-to-end request encryption for web applications.

- **Load Autoscaling:** Adjust capacity dynamically as web traffic load changes.


    