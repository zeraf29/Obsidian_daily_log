

--- 
author: zeraf29
created: 2023-11-10 08:45 
last-updated: 2023-11-10 08:45 
summaries: 
tags:

---


## Memo



**App Service plan** and **Consumption plan** are two different hosting options for Azure App Service. The main difference between the two is that App Service plans are dedicated resources, while Consumption plans are serverless.

**App Service plan**

- Dedicated resources: App Service plans provide dedicated resources for your app, such as CPU, memory, and storage. This means that you have complete control over the resources that your app uses.
- Predictable pricing: App Service plans have predictable pricing, so you can budget for your hosting costs.
- Features: App Service plans offer a variety of features, such as custom domains, SSL certificates, and continuous integration and delivery (CI/CD).

**Consumption plan**

- Serverless: Consumption plans are serverless, which means that you don't have to manage any infrastructure. Azure automatically scales your app up or down based on demand.
- Pay-as-you-go pricing: Consumption plans are billed based on the resources that your app consumes. This means that you only pay for what you use.
- Features: Consumption plans offer a limited set of features, but they are sufficient for many simple apps.

**Comparison table**

|Feature|App Service plan|Consumption plan|
|---|---|---|
|Resources|Dedicated|Serverless|
|Pricing|Predictable|Pay-as-you-go|
|Features|Full set|Limited set|
|Use cases|Complex apps, apps with high traffic, apps with specific resource requirements|Simple apps, apps with low traffic, apps with unpredictable traffic|

Sheets로 내보내기

**Which plan should you choose?**

The best plan for you will depend on your specific needs. If you need dedicated resources, predictable pricing, and a full set of features, then you should choose an App Service plan. If you are looking for a cost-effective and easy-to-manage solution for a simple app, then you should choose a Consumption plan.

Here are some additional things to consider when choosing between an App Service plan and a Consumption plan:

- **Traffic:** If you expect your app to have high traffic, then you should choose an App Service plan. This will ensure that your app has the resources it needs to handle the load.
- **Scalability:** If you need your app to scale automatically, then you should choose a Consumption plan. Consumption plans can scale up or down based on demand, so you don't have to worry about managing your infrastructure.
- **Features:** If you need specific features that are not available in the Consumption plan, such as custom domains or SSL certificates, then you should choose an App Service plan.

If you are still unsure which plan to choose, you can contact Microsoft support for assistance.
