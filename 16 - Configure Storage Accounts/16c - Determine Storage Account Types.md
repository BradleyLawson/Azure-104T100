# Determine Storage Account Types

**Objective:** Azure Storage offers several storage account options, each tailored to different use cases, services, and pricing models.

## Storage Account Types

### Standard General-Purpose v2

- **Supported Services:** Blob Storage (including Data Lake Storage), Queue Storage, Table Storage, and Azure Files.
- **Recommended Usage:** This is the standard storage account for most scenarios. It supports various services, including blobs, file shares, queues, tables, and disks (page blobs). It's suitable for most general use cases.

### Premium Block Blobs

- **Supported Services:** Blob Storage (including Data Lake Storage).
- **Recommended Usage:** Premium storage account specifically designed for block blobs and append blobs. It is ideal for applications with high transaction rates. Choose Premium block blobs if you work with smaller objects or require consistently low storage latency. This storage type is built to scale with your applications.

### Premium File Shares

- **Supported Services:** Azure Files.
- **Recommended Usage:** Premium storage account exclusively for file shares. It's recommended for enterprise or high-performance scale applications. Opt for Premium file shares if you need support for both Server Message Block (SMB) and NFS file shares.

### Premium Page Blobs

- **Supported Services:** Page blobs only.
- **Recommended Usage:** Premium high-performance storage account designed specifically for page blobs. Page blobs are suitable for storing index-based and sparse data structures, such as operating systems, data disks for virtual machines, and databases.

> **Note:** All storage account types ensure data at rest is encrypted using Storage Service Encryption (SSE).
