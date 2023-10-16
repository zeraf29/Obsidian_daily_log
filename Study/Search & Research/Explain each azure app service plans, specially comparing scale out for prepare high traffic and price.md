

--- 
author: zeraf29
created: 2023-10-17 08:29 
last-updated: 2023-10-17 08:29 
summaries: 
tags:

---


## Memo


The Azure App Service shared tier is a special tier that is designed for development and testing purposes. It is not suitable for production apps, as it does not offer any performance guarantees or SLA.

The shared tier does not support scale out, so all traffic to your app will be handled by a single instance. This means that if your app experiences a sudden spike in traffic, it will likely become unavailable.

If you are expecting high traffic to your app, then you should not use the shared tier. You should instead choose a higher-priced plan that supports scale out, such as the Standard or Premium plan.

**Here is a table comparing the different App Service plans, with a focus on scale out for high traffic and price:**

|App Service plan|Scale out|Price|
|---|---|---|
|Shared|No|Lowest|
|Basic|No|Low|
|Standard|Yes, up to 20 instances|Moderate|
|Premium|Yes, up to 100 instances|Highest|

Sheets로 내보내기

**Recommendation:**

If you are expecting high traffic to your app, then you should not use the shared tier. You should instead choose a higher-priced plan that supports scale out, such as the Standard or Premium plan.

The Standard plan is a good option for most apps, as it offers a good balance of performance, scalability, and price. However, if you are expecting very high traffic, then you may want to choose the Premium plan, which offers the best performance and scalability. 
