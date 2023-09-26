# Determine Replication Strategies

**Objective:** Azure Storage offers various replication strategies to ensure data durability and high availability in different scenarios.

## Replication Strategies

### Locally Redundant Storage (LRS)

- **Description:** The lowest-cost replication option with the least durability. Data is replicated within the same data center.
- **Use Cases:** Suitable when data loss can be easily reconstructed, data is constantly changing and not essential, or data governance requires replication within a country/region.

### Zone Redundant Storage (ZRS)

- **Description:** Synchronously replicates data across three storage clusters in a single region, each in its own availability zone.
- **Use Cases:** Ensures access and management of data if a zone becomes unavailable. Provides excellent performance and low latency.

### Geo-Redundant Storage (GRS)

- **Description:** Replicates data to a secondary region hundreds of miles away, ensuring higher durability even during regional outages.
- **Use Cases:** Designed for critical data. Provides at least 99.99999999999999% (16 9's) durability. Offers read-access options in the secondary region.

### Geo-Zone-Redundant Storage (GZRS)

- **Description:** Combines the high availability of ZRS with protection from regional outages as in GRS. Replicates data across Azure availability zones and secondary regions.
- **Use Cases:** Ideal for applications requiring consistency, durability, high availability, and resilience for disaster recovery. Offers read access to a secondary region.

## Considerations for Choosing Replication Strategies

When choosing replication strategies, consider various factors, including node unavailability, data center unavailability, region-wide outages, read access during region-wide outages, and supported storage account types. Here's a summary:

| Node in Data Center Unavailable | Entire Data Center Unavailable | Region-Wide Outage | Read Access During Region-Wide Outage | Supported Storage Accounts |
|---------------------------------|---------------------------------|--------------------|-------------------------------------|---------------------------|
| LRS, ZRS, GRS, RA-GRS, GZRS, RA-GZRS | ZRS, GRS, RA-GRS, GZRS, RA-GZRS | GRS, RA-GRS, GZRS, RA-GZRS | RA-GRS, RA-GZRS | LRS: GPv1, GPv2, Blob; ZRS: GPv2; GRS: GPv1, GPv2, Blob; RA-GRS: GPv1, GPv2, Blob; GZRS: GPv2; RA-GZRS: GPv2 |
