# Create Public IP Addressing

In Azure, you can easily create a public IP address for your resources using the Azure portal. This public IP address allows your resource to communicate with the internet and external services.

![Screenshot: Create a Public IP Address](insert_screenshot_link_here)

## Important Considerations

When creating a public IP address, there are several settings to configure:

### IP Version

You can choose to create an IPv4 address, an IPv6 address, or both (IPv4 and IPv6). Select the option that suits your needs. If you choose both, you'll create two public IP addresses, one for IPv4 and one for IPv6.

### SKU (Stock Keeping Unit)

Select the SKU for the public IP address. You can choose between "Basic" and "Standard." Ensure that the SKU matches the Azure load balancer with which the public IP address will be used.

### Name

Enter a unique name to identify the IP address. This name should be unique within the resource group you select for this IP address.

### IP Address Assignment

There are two types of IP address assignments:

#### Dynamic IP Addresses

- Dynamic addresses are assigned after a public IP address is associated with an Azure resource and the resource is started for the first time.
- Dynamic addresses can change if the resource (e.g., a virtual machine) is stopped and then restarted via Azure. However, the address remains the same if the resource is rebooted or stopped from within the guest operating system.
- When you remove a public IP address resource from a resource, the dynamic address is released.

#### Static IP Addresses

- Static addresses are assigned when a public IP address is created.
- These addresses remain unchanged until the public IP address resource is deleted.
- If the address is not associated with a resource, you can change the assignment method after the address is created. However, if the address is associated with a resource, changing the assignment method might not be possible.

**Note**: If you choose IPv6 as the IP version, you must use the Dynamic assignment method for the Basic SKU. The Standard SKU provides Static addresses for both IPv4 and IPv6.

Creating a public IP address is a straightforward process in Azure and is essential for enabling communication between your resources and the internet.
