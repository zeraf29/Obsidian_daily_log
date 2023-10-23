

--- 
author: zeraf29
created: 2023-10-24 08:37 
last-updated: 2023-10-24 08:37 
summaries: 
tags:

---


## Memo

**A. File Storage**

OCI File Storage is a highly scalable, shared file system that provides durable, secure, and high-performance storage for applications and workloads that require access to file-based data. It is a good choice for storing and accessing data that needs to be shared across multiple compute instances or applications, such as home directories, shared workspaces, and application data.

File Storage is durable and reliable, with a high availability of 99.999999999%. It also offers a variety of security features, such as encryption, access control, and audit logging.

File Storage is available in two tiers:

- **Standard:** The Standard tier is a good choice for most workloads, as it offers a good balance of performance and cost.
- **High Performance:** The High Performance tier is designed for workloads that require high throughput and low latency, such as video streaming and gaming.

**B. Object Storage (standard)**

OCI Object Storage is an object storage service that provides highly scalable, secure, and durable storage for any kind of data. It is a good choice for storing and accessing large amounts of data, such as backups, archives, and web content.

Object Storage is extremely scalable and can be used to store petabytes of data. It is also very secure, with a variety of security features such as encryption, access control, and audit logging.

Object Storage is available in three tiers:

- **Standard:** The Standard tier is the most cost-effective tier and is a good choice for most workloads.
- **Infrequent Access:** The Infrequent Access tier is designed for data that is accessed less frequently, such as archives and backups.
- **Archive:** The Archive tier is designed for data that is rarely accessed, such as historical data and compliance records.

**C. Archive Storage**

OCI Archive Storage is a low-cost, highly durable storage service for long-term data retention. It is a good choice for storing data that needs to be retained for compliance or regulatory reasons, or for historical data that is rarely accessed.

Archive Storage is very durable, with a data durability of 99.999999999%. It is also very secure, with a variety of security features such as encryption, access control, and audit logging.

**D. Block Volume**

OCI Block Volume is a high-performance block storage service that provides durable, secure, and scalable storage for compute instances. It is a good choice for storing and accessing data that needs to be accessed frequently, such as database files, operating systems, and application data.

Block Volume is highly scalable and can be used to store petabytes of data. It is also very secure, with a variety of security features such as encryption, access control, and audit logging.

Block Volume is available in two tiers:

- **Standard:** The Standard tier is a good choice for most workloads, as it offers a good balance of performance and cost.
- **High Performance:** The High Performance tier is designed for workloads that require very high performance, such as online transaction processing (OLTP) databases and high-performance computing (HPC) applications.

**Which OCI storage service should I use?**

The best OCI storage service for you will depend on your specific needs. If you need to store and access large amounts of data, such as backups, archives, and web content, then Object Storage is a good choice. If you need to store and access data that needs to be accessed frequently, such as database files, operating systems, and application data, then Block Volume is a good choice. If you need to store data that needs to be retained for long-term data retention, then Archive Storage is a good choice.

You can also use a combination of OCI storage services to meet your needs. For example, you could use Block Volume to store your operating system and application data, and Object Storage to store your backups and archives.



