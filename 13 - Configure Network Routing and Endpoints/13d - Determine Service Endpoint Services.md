# Determining Service Endpoint Services 

Adding a service endpoint to your virtual network is a straightforward process. In the Azure portal, you can select the Azure service for which you want to create the endpoint. In this unit, we'll explore several services, including Azure Cosmos DB, Event Hubs, Key Vault, and SQL Database.

**Note**: Adding service endpoints may take up to 15 minutes to complete. Each service endpoint integration has its dedicated Azure documentation page.

## Key Azure Service Endpoints

Let's take a look at some key Azure service endpoints:

### Azure Storage
- **Availability**: Generally available in all Azure regions.
- **Description**: This endpoint provides an optimized route for traffic to the Azure Storage service. Each Storage account can support up to 100 virtual network rules.

### Azure SQL Database and Azure SQL Data Warehouse
- **Availability**: Generally available in all Azure regions.
- **Description**: These services offer a firewall security feature that controls whether your database accepts communication from specific subnets in virtual networks. This feature applies to the database server for your single databases and elastic pool in SQL Database or your databases in SQL Data Warehouse.

### Azure Database for PostgreSQL and Azure Database for MySQL
- **Availability**: Generally available in Azure regions where the database service is available.
- **Description**: Virtual network service endpoints and rules extend the private address space of a virtual network to your Azure Database for PostgreSQL server and Azure Database for MySQL server.

### Azure Cosmos DB
- **Availability**: Generally available in all Azure regions.
- **Description**: You can configure Azure Cosmos DB accounts to allow access only from a specific subnet within a virtual network. Enabling service endpoints grants access to Azure Cosmos DB from that subnet, ensuring traffic is sent with the subnet and virtual network's identity. After enabling the Azure Cosmos DB service endpoint, you can limit access to the specified subnet in your Azure Cosmos DB account.

### Azure Key Vault
- **Availability**: Generally available in all Azure regions.
- **Description**: Virtual network service endpoints for Key Vault enable you to restrict access to a designated virtual network. They also allow you to limit access to a list of IPv4 address ranges. Users attempting to connect to your Key Vault from outside these sources will be denied access.

### Azure Service Bus and Azure Event Hubs
- **Availability**: Generally available in all Azure regions.
- **Description**: Integrating Service Bus with virtual network service endpoints ensures secure access to messaging capabilities from workloads like virtual machines connected to virtual networks. The network traffic path is secured on both ends.

These service endpoints enhance the security and accessibility of Azure services, making them valuable tools in configuring your Azure environment.
