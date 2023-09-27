# Identify Domains and Custom Domains

Azure DNS allows you to host your DNS domains within Azure, providing name resolution for your domains using Microsoft Azure infrastructure. You can configure and manage custom domains with Azure DNS through the Azure portal. This approach allows you to use the same credentials, support agreements, and billing preferences as your other Azure services.

## Key Concepts about Domain Names in Azure

Before you begin using Azure DNS to host DNS records for your domains, there are some important concepts to understand:

### 1. Initial Domain Name

- When you create an Azure subscription, Azure automatically generates an Azure Active Directory (Azure AD) domain associated with your subscription.

- The initial domain name for this Azure AD domain follows the format `<Your Domain Name>.onmicrosoft.com`. For example, if your organization is named "Your Domain Name," the initial domain name might be `yourdomainname.onmicrosoft.com`.

- It's worth noting that you must be a global administrator to perform domain management tasks within Azure AD.

### 2. Custom Domain Names

- Custom domain names are used to provide a more user-friendly and simplified form of your domain name for specific users or tasks.

- Organizations often implement custom domain names to allow users to access their domain using familiar credentials.

- For example, if your initial Azure AD domain name is `azureadminincorg.onmicrosoft.com`, you can create a custom domain name like `azureadmininc.org` for a more user-friendly experience.

### 3. Verification of Custom Domain Names

- Before a custom domain name can be used within Azure AD, it must be added to your directory and verified.

- The initial domain name, in the format `<Your Domain Name>.onmicrosoft.com`, is intended to be used until your custom domain name is verified.

- The initial domain name cannot be changed or deleted, but you have the flexibility to add a routable custom domain name that you control.

- It's important to note that domain names within Azure AD must be globally unique. Once a specific domain name is verified in one Azure AD directory, it cannot be used by other Azure AD directories.

These concepts lay the foundation for managing and customizing domain names within Azure, ensuring a seamless experience for your organization and users.
