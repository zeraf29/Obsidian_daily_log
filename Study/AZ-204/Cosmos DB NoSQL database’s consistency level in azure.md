

--- 
author: zeraf29
created: 2023-11-16 08:46 
last-updated: 2023-11-16 08:46 
summaries: 
tags:

---


## Memo

In Azure Cosmos DB, consistency levels define the guarantees that read and write operations will return the most up-to-date data. Different consistency levels offer varying degrees of consistency and performance trade-offs.

Here's an overview of the five consistency levels available in Azure Cosmos DB:

1. **Strong Consistency:** Strong consistency ensures that every read operation will always return the most recent write operation, regardless of where the read and write operations occur. It provides the highest level of data consistency but has the highest latency and throughput cost.
    
2. **Bounded Staleness (Session Consistency):** Bounded staleness guarantees that read operations will return the most recent write operation within a specified time window. This time window is known as the staleness limit and is typically measured in seconds. Bounded staleness offers a balance between consistency and performance, making it a popular choice for many applications.
    
3. **Consistent Prefix (Eventual Consistency):** Consistent prefix guarantees that all reads after a write operation will always see the effects of that write, but it does not guarantee that all reads will see the most recent write. Eventual consistency offers the lowest latency and throughput cost but may have a short period of inconsistency after writes occur.
    
4. **Session (Session Token):** Session consistency guarantees that all reads within a session will see the same data. Sessions are created and managed by the application and are typically associated with a specific user or task. Session consistency offers a balance between consistency and performance, making it suitable for applications that require consistent data views within a session.
    
5. **Eventual Consistency (Last Write Wins):** Eventual consistency ensures that all reads will eventually see the most recent write operation, but it does not guarantee a specific timeframe for this. It offers the lowest latency and throughput cost but may have the longest period of inconsistency after writes occur.
    

The choice of consistency level depends on the specific requirements of the application. For applications that require strict data consistency at all times, strong consistency or bounded staleness may be appropriate. For applications that prioritize performance and can tolerate a short period of inconsistency, eventual consistency or session consistency may be suitable.

Here's a summary table of the consistency levels:

|Consistency Level|Guarantees|Performance|
|---|---|---|
|Strong Consistency|Every read returns the most recent write|Lowest latency, lowest throughput|
|Bounded Staleness|Reads return the most recent write within a specified time window|Moderate latency, moderate throughput|
|Consistent Prefix|Reads after a write see the effects of that write|High latency, high throughput|
|Session|Reads within a session see the same data|Moderate latency, moderate throughput|
|Eventual Consistency|All reads eventually see the most recent write|Highest latency, highest throughput|

Sheets로 내보내기

Remember, the optimal consistency level depends on the specific needs and trade-offs of your application.


