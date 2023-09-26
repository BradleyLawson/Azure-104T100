# Azure Application Gateway Routing

**Objective:** Clients send requests to your web apps through your Application Gateway, which then directs the requests to specific web servers based on predefined rules.

## Traffic Routing Options

When it comes to routing traffic with Azure Application Gateway, there are two primary methods:

1. **Path-Based Routing:** This method directs requests with different URL paths to different groups of back-end servers. For instance, you can send requests for `/video/*` to servers optimized for video streaming and requests for `/images/*` to servers designed for image retrieval.

2. **Multi-Site Routing:** Multi-site routing is useful when you need to support multiple web apps on the same Application Gateway instance. It's commonly used for multi-tenant applications, where each tenant has its own set of resources hosting a web application. In this setup, you register multiple DNS names (CNAMEs) for the IP address of your Application Gateway and specify the name of each site. Application Gateway uses separate listeners for each site and routes requests to different back-end pools.

## Additional Routing Features

Azure Application Gateway offers some advanced routing features:

- **Traffic Redirection:** You can configure the gateway to redirect traffic from one listener to another or to an external site. This is often used to automatically redirect HTTP requests to HTTPS for enhanced security.

- **HTTP Header Rewriting:** Modify HTTP headers to translate URLs or query string parameters and adjust request and response headers. You can apply conditions to rewrite headers selectively.

- **Custom Error Pages:** Instead of displaying default error pages, you can create custom error pages with your own branding and layout to enhance the user experience.
