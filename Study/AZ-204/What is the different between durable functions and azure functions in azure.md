

--- 
author: zeraf29
created: 2023-11-07 08:40 
last-updated: 2023-11-07 08:40 
summaries: 
tags:

---


## Memo

Azure Functions is a serverless computing service that lets you run code on demand without provisioning or managing servers. Azure Durable Functions is an extension of Azure Functions that lets you write stateful functions in a serverless compute environment.

The main difference between Azure Functions and Azure Durable Functions is that Azure Durable Functions functions can maintain state between executions. This is possible because Durable Functions uses a durable storage mechanism, such as Azure Storage, to persist state data.

Another difference between the two is that Azure Durable Functions provides a number of features that make it suitable for building long-running workflows, such as checkpointing, restarting, and orchestration.

Here is a table that summarizes the key differences between Azure Functions and Azure Durable Functions:

|Feature|Azure Functions|Azure Durable Functions|
|---|---|---|
|Stateful|No|Yes|
|Long-running workflows|No|Yes|
|Checkpointing|No|Yes|
|Restarting|No|Yes|
|Orchestration|No|Yes|

Sheets로 내보내기

**When to use Azure Functions:**

- When you need to run short-running, stateless functions.
- When you need to respond to events quickly.
- When you need to scale your code horizontally.

**When to use Azure Durable Functions:**

- When you need to write stateful functions.
- When you need to build long-running workflows.
- When you need to process large volumes of data.

Here are some examples of scenarios where you might want to use Azure Durable Functions:

- Order processing system.
- Real-time analytics pipeline.
- IoT device management system.
- Document processing system.

Overall, Azure Durable Functions is a powerful extension of Azure Functions that lets you write reliable and scalable code to handle complex workflows and large volumes of data.


