

--- 
author: zeraf29
created: 2023-10-16 08:42 
last-updated: 2023-10-16 08:42 
summaries: 
tags:

---


## Memo
-

In Microsoft Azure Functions, **perpetually warm instances** are instances that are always kept running and ready to serve requests. This means that there is no cold start penalty when a request is received, and the function can start processing the request immediately.

Perpetually warm instances are available in the Azure Functions Premium plan. This plan is designed for functions that need to be highly responsive and have low latency.

There are several benefits to using perpetually warm instances in Azure Functions:

- **Improved performance:** Perpetually warm instances can improve the performance of your Azure Functions apps by eliminating the cold start penalty. This is especially important for functions that are triggered by events, such as HTTP requests or messages from a queue.
- **Increased reliability:** Perpetually warm instances can help to improve the reliability of your Azure Functions apps by ensuring that they are always ready to serve requests. This is important for functions that are used to support critical business processes.
- **Reduced costs:** Perpetually warm instances can help to reduce the costs of your Azure Functions apps by eliminating the need to scale up the number of instances when traffic increases. This is because the perpetually warm instances are always ready to serve requests.

To use perpetually warm instances in Azure Functions, you need to create a function app with the Premium plan. You can then configure the number of perpetually warm instances that you want to use.

Here are some examples of when you might want to use perpetually warm instances in Azure Functions:

- Functions that are triggered by HTTP requests, such as APIs or webhooks.
- Functions that are used to support critical business processes, such as order processing or customer support.
- Functions that need to have low latency, such as real-time data processing or streaming analytics.

If you are looking for a way to improve the performance, reliability, and cost-effectiveness of your Azure Functions apps, then using perpetually warm instances is a good option to consider.

