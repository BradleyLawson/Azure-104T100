# Access Storage in Azure

**Objective:** Learn how to access objects in Azure Storage and configure custom domains.

## Accessing Storage

Every object stored in Azure Storage has a unique URL address, with the storage account name forming the subdomain portion of the URL. The combination of the subdomain and the domain name forms an endpoint for your storage account. Here's an example for a storage account named `mystorageaccount`:

- Container service: `//mystorageaccount.blob.core.windows.net`
- Table service: `//mystorageaccount.table.core.windows.net`
- Queue service: `//mystorageaccount.queue.core.windows.net`
- File service: `//mystorageaccount.file.core.windows.net`

To access an object in your storage account, you append the object's location to the endpoint. For example, to access `myblob` data in the `mycontainer` location:

`//mystorageaccount.blob.core.windows.net/mycontainer/myblob`

## Configuring Custom Domains

You can configure a custom domain to access blob data in your Azure storage account. Azure Storage doesn't natively support HTTPS with custom domains, so you can implement an Azure Content Delivery Network (CDN) for HTTPS support.

There are two ways to configure a custom domain:

1. **Direct Mapping:** Enables a custom domain for a subdomain to an Azure storage account by creating a CNAME record. Example:
   - Subdomain: `blobs.contoso.com`
   - Azure storage account: `<storage account>.blob.core.windows.net`
   - Direct CNAME record: `contosoblobs.blob.core.windows.net`

2. **Intermediary Domain Mapping:** Applied to a domain already in use within Azure, which may result in minor downtime. To avoid downtime, you can use the `asverify` intermediary domain to validate the domain. Example:
   - CNAME record: `asverify.blobs.contoso.com`
   - Intermediate CNAME record: `asverify.contosoblobs.blob.core.windows.net`

By following these steps, you can configure custom domains to access blob data in your Azure storage account.
