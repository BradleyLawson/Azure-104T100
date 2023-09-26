# Secure Storage Endpoints in Azure

**Objective:** Learn how to configure secure service endpoints and restrict network access for your Azure storage account.

## Configuring Service Endpoints

In the Azure portal, each Azure service requires specific steps to configure service endpoints and control network access. To access these settings for your storage account, you'll utilize the "Firewalls and virtual networks" settings. This allows you to specify which virtual networks should have access to the service for the account.

### Key Points to Consider

Here are some important points to keep in mind when configuring service access settings:

- The "Firewalls and virtual networks" settings enable you to restrict access to your storage account from specific subnets on virtual networks or public IPs.

- You have the option to configure the service to allow access from one or more public IP ranges.

- Subnets and virtual networks must exist in the same Azure region or region pair as your storage account.

It's crucial to thoroughly test the service endpoint and verify that it limits access as expected to ensure the security of your Azure storage account.
