# Implement Azure Storage

**Objective:** Azure Storage is Microsoft's cloud storage solution, offering scalable storage options for various data types. It serves as a foundation for modern data storage scenarios.

## Key Points

### What is Azure Storage?

Azure Storage is a versatile service designed for storing files, messages, tables, and more. It is used in various applications, including file shares, websites, mobile apps, and desktop applications. Additionally, Azure Storage is employed by both Infrastructure as a Service (IaaS) virtual machines and Platform as a Service (PaaS) cloud services.

### Three Categories of Data

Azure Storage supports three categories of data:

1. **Virtual Machine Data:** This includes disks and files. Disks provide persistent block storage for Azure IaaS virtual machines, while files offer fully managed file shares in the cloud. The number of data disks you can add depends on the virtual machine size, and each data disk has a maximum capacity of 32,767 GB.

2. **Unstructured Data:** Unstructured data is less organized and lacks a clear relationship. It can be a mix of information stored together. Azure Blob Storage and Azure Data Lake Storage are used to store unstructured data. Blob Storage is a highly scalable cloud object store, while Azure Data Lake Storage serves as a Hadoop Distributed File System (HDFS) as a service.

3. **Structured Data:** Structured data is organized in a relational format with a shared schema. It is often found in database tables with rows, columns, and keys. Azure Table Storage, Azure Cosmos DB, and Azure SQL Database are used to store structured data. Azure Cosmos DB is a globally distributed database service, and Azure SQL Database is a fully managed database-as-a-service built on SQL.

### Storage Account Tiers

Azure storage accounts come in two tiers:

- **Standard Storage Accounts:** Backed by magnetic hard disk drives (HDD), these provide cost-effective storage for applications that require bulk storage or infrequently accessed data.

- **Premium Storage Accounts:** Backed by solid-state drives (SSD), these offer consistent low-latency performance and are suitable for Azure virtual machine disks with I/O-intensive applications like databases.

### Considerations for Azure Storage

When planning your Azure Storage configuration, consider the following features:

- **Durability and Availability:** Azure Storage ensures data durability and availability through redundancy across datacenters or geographical regions. This protects your data from hardware failures, local catastrophes, or natural disasters.

- **Secure Access:** All data written to Azure Storage is encrypted. You have fine-grained control over who can access your data.

- **Scalability:** Azure Storage is designed to handle the storage and performance needs of modern applications with massive scalability.

- **Manageability:** Microsoft Azure takes care of hardware maintenance, updates, and critical issues for you.

- **Data Accessibility:** Data stored in Azure Storage is accessible worldwide over HTTP or HTTPS. Microsoft provides SDKs in various languages, including .NET, Java, Node.js, Python, PHP, Ruby, Go, and REST APIs. You can also use Azure PowerShell, Azure CLI, Azure portal, and Azure Storage Explorer for data management.
