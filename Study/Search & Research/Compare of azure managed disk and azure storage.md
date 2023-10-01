

--- 
author: zeraf29
created: 2023-09-20 08:45 
last-updated: 2023-09-20 08:45 
summaries: 
tags:

---

## Memo
Azure managed disks and Azure storage are both durable and scalable storage solutions for Azure workloads. However, there are some key differences between the two.

**Azure managed disks** are block-level storage volumes that are managed by Azure and used with Azure Virtual Machines. Managed disks provide high performance, durability, and availability for Azure VMs. They are also easy to use and manage, as Azure takes care of all the underlying storage management tasks.

**Azure storage** is a cloud storage service that provides a variety of storage options, including blob storage, disk storage, file storage, and queue storage. Azure storage can be used to store a wide variety of data, including application data, media files, and backup data. Azure storage is also highly scalable and can be used to store data up to petabytes in size.

Here is a table that summarizes the key differences between Azure managed disks and Azure storage:

|Feature|Azure managed disks|Azure storage|
|---|---|---|
|Type of storage|Block storage|Object storage, disk storage, file storage, and queue storage|
|Use case|For use with Azure Virtual Machines|For storing a wide variety of data, including application data, media files, and backup data|
|Management|Managed by Azure|Managed by the customer|
|Performance|High performance|Good performance|
|Durability|Durable|Durable|
|Availability|High availability|High availability|
|Scalability|Scalable|Highly scalable|

Sheets로 내보내기

**Which one should you use?**

The best choice for you will depend on your specific needs. If you are running Azure Virtual Machines, then Azure managed disks are the best choice. Managed disks are optimized for Azure VMs and provide high performance, durability, and availability.

If you need to store a wide variety of data, including application data, media files, and backup data, then Azure storage is the best choice. Azure storage is also a good choice if you need to store large amounts of data or if you need to store data in a specific region or country.

You can also use Azure managed disks and Azure storage together. For example, you could use Azure managed disks to store the operating system and application data for your Azure VMs, and you could use Azure storage to store backup data or media files.

#### 출처

[](https://bard.google.com/faq#citation)

1. [23819s66e64l.poligraf-groups.ru/](http://23819s66e64l.poligraf-groups.ru/)




Here is a table that compares the redundancy options for Azure managed disks and Azure storage:

|Storage type|Redundancy options|
|---|---|
|Azure managed disks|Locally redundant storage (LRS), zone-redundant storage (ZRS)|
|Azure storage|Locally redundant storage (LRS), zone-redundant storage (ZRS), geo-redundant storage (GRS), geo-zone-redundant storage (GZRS)|

Sheets로 내보내기

**Locally redundant storage (LRS)**

LRS replicates your data three times within a single physical location in the region. This means that your data is protected against hardware failures, but it is not protected against a major outage in the entire region.

**Zone-redundant storage (ZRS)**

ZRS synchronously replicates your data across three Azure availability zones in the region you select. Each availability zone is a separate physical location with its own power, cooling, and networking infrastructure. This means that your data is protected against hardware failures and regional outages.

**Geo-redundant storage (GRS)**

GRS replicates your data synchronously three times within a single physical location in the primary region using locally redundant storage (LRS), and then asynchronously replicates it to a secondary region that is hundreds of miles away. This means that your data is always protected, even if there is a major outage in the primary region.

**Geo-zone-redundant storage (GZRS)**

GZRS synchronously replicates your data across three Azure availability zones in the primary region, and then asynchronously replicates it to a secondary region that is hundreds of miles away. This means that your data is protected against hardware failures, regional outages, and even a major outage in the entire primary region.

**Which redundancy option should you choose?**

The best redundancy option for you will depend on your specific needs. If you need the highest level of data protection and availability, then you should choose geo-zone-redundant storage (GZRS). However, GZRS is also the most expensive redundancy option.

If you need a high level of data protection and availability, but you are on a budget, then you can choose geo-redundant storage (GRS). GRS is less expensive than GZRS, but it does not protect your data against a major outage in the entire primary region.

If you need a good level of data protection and availability, but you do not need the same level of protection as GRS or GZRS, then you can choose zone-redundant storage (ZRS). ZRS is more expensive than LRS, but it does protect your data against regional outages.

If you are on a tight budget, then you can choose locally redundant storage (LRS). LRS is the least expensive redundancy option, but it does not protect your data against a major outage in the entire region.

It is important to note that no redundancy option can protect your data against accidental deletion or modification. You should always use backups to protect your data against these types of events.

#### 출처

[](https://bard.google.com/faq#citation)

1. [github.com/MicrosoftDocs/azure-docs/blob/main/articles/virtual-machines/disks-redundancy.md](https://github.com/MicrosoftDocs/azure-docs/blob/main/articles/virtual-machines/disks-redundancy.md) 
~