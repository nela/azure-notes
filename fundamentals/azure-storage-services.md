# Azure Storage Services Fundamentals

Notes for [Azure Storage Service Fundamentals](https://docs.microsoft.com/en-us/learn/modules/azure-storage-fundamentals/).

Core Storage Services:

- Disk Storage
- Object Store
- Filesystem Service for the Cloud
- Messaging store
- NoSQL

## Azure Disk Storage

- Disk storage provides disks for Azure VMs, allows data to be persistently
stored and accessed from an attached virtual hard disk.
  - Azure VMs use Azure Disk Storage to store virtual disks. However, you can't
  use Azure Disk Storage to store a disk outside of a virtual machine.

Performance tiers:
- Standard SSD & HDD for less critical workloads
- Premium SSD disks for mission-critical production apps
- Ultra Disks for data-intensive workloads such as SAP HANA, top tier
databases, transaction-heavy workloads.

## Azure Blob Storage

Object storage solution for the cloud. Stores massive amounts of data such as
text or binary data. Blob storage is unstructured, meaning that there are no
restrictions on the kinds of data it can holds; can contain GBs of binary data,
encrypted messages for another application, or data in custom format.

Ideal for:
- Serving images or documents directly to a browser
- Storing files for distributed access
- Streaming video and audio
- Storing data for backup and restore, disaster recovery, and archiving
- Storing data for analysis by an on-prem or Azure-hosted service
- Storing up to 8 TB for VMs.

## Azure Files

Fully managed file shares in the cloud accessible via Server Message Block and
Network File System (preview?) protocols. Apps running in a VM or cloud
services can mount a file storage share to access file data.

**Access**

Accessible from anywhere in the world, by using a URL pointing to a file.
_Shared Access Signature_ (SAS) tokens allow access to a private asset for
a specific amount of time.

Ideal for:
- Migration of applications using file shares. Mount the Azure file share to
the same Drive letter as the on-premise application uses.
- Store configuration files on a file share and access them from multiple VMs.
Tools and utilities used by multiple devs in group can be stored on a file
share.
- Write data to a file share, process or analyse later, e.g. Diagnostic logs,
  metrics, crash dumps.

## Blob Access Tiers

- **Hot**: Optimized for storing data that is accessed frequently.
- **Cool**: Optimized for data that is infrequently accessed and stored for at least 30 days.
- **Archive**: Appropriate for data that is rarely accessed and stored for at least 180 days, with flexible latency requirements.

Considerations:
- Only the hot and cool access tiers can be set at the account level. The
  archive access tier isn't available at the account level.
- Hot, cool, and archive tiers can be set at the blob level, during upload or
after upload. (What does during or after upload mean?)
- Cool tier can tolerate slightly lower availability, but still requires high
durability, retrieval latency, throughput similar to hot data. Slightly lower
availability SLA and higher access costs compared to hot data.
- Archive storage stores data offline and offers lowest costs, but highest cost
to rehydrate(?) and access data.
