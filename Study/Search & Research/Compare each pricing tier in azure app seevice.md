

--- 
author: zeraf29
created: 2023-09-21 08:27 
last-updated: 2023-09-21 08:27 
summaries: 
tags:

---


## Memo

The following table compares the network environment of each Azure App Service pricing tier:

| Pricing tier | Network environment | |---|---|---| | Free | Public network only | | Shared | Public or private network | | Basic | Public or private network | | Standard | Public or private network, with dedicated outbound IP addresses | | Premium | Public or private network, with dedicated inbound and outbound IP addresses |

**Free tier**

The Free tier is the most basic App Service tier. It is designed for development and testing purposes. The Free tier apps are hosted on shared servers and are accessible only from the public internet.

**Shared tier**

The Shared tier is a good option for low-traffic websites and apps. Shared tier apps are hosted on shared servers, but they can be configured to be accessed from either the public internet or a private network.

**Basic tier**

The Basic tier is a good option for medium-traffic websites and apps. Basic tier apps are hosted on dedicated servers and can be configured to be accessed from either the public internet or a private network.

**Standard tier**

The Standard tier is a good option for high-traffic websites and apps. Standard tier apps are hosted on dedicated servers and have dedicated outbound IP addresses. This can improve performance and security.

**Premium tier**

The Premium tier is the most expensive App Service tier. It is designed for high-traffic and mission-critical websites and apps. Premium tier apps are hosted on dedicated servers and have dedicated inbound and outbound IP addresses. This can improve performance and security.

**Network environment**

The network environment of an App Service app is the network that the app is accessible from. The network environment can be either public or private.

- **Public network:** A public network is a network that is accessible from the internet.
- **Private network:** A private network is a network that is not accessible from the internet.

**Choosing a pricing tier**

The best pricing tier for your App Service app depends on your needs and requirements. Consider the following factors when choosing a pricing tier:

- **Traffic volume:** How much traffic does your app expect to receive?
- **Performance:** How important is performance for your app?
- **Security:** How important is security for your app?
- **Network environment:** Do you need your app to be accessible from the public internet or a private network?

Once you have considered these factors, you can choose the pricing tier that best meets your needs.



The Isolated and Consumption pricing tiers are both premium tiers that offer dedicated hosting and dedicated inbound and outbound IP addresses.

**Isolated tier**

The Isolated tier is a good option for high-traffic and mission-critical websites and apps that require a high level of security and isolation. Isolated tier apps are hosted in dedicated App Service environments, which are isolated from other App Service environments and the public internet.

**Consumption tier**

The Consumption tier is a good option for high-traffic and mission-critical websites and apps that require a high level of scalability and elasticity. Consumption tier apps are hosted in a shared App Service environment, but they are scaled up or down automatically based on demand.

**Network environment**

The network environment of an Isolated or Consumption tier App Service app can be either public or private.

- **Public network:** A public network is a network that is accessible from the internet.
- **Private network:** A private network is a network that is not accessible from the internet.

**Choosing a pricing tier**

The best pricing tier for your App Service app depends on your needs and requirements. Consider the following factors when choosing a pricing tier:

- **Traffic volume:** How much traffic does your app expect to receive?
- **Performance:** How important is performance for your app?
- **Security:** How important is security for your app?
- **Network environment:** Do you need your app to be accessible from the public internet or a private network?
- **Scalability:** How important is scalability for your app?
- **Elasticity:** How important is elasticity for your app?

Once you have considered these factors, you can choose the pricing tier that best meets your needs.

**Difference between Isolated and Consumption tiers**

The main difference between the Isolated and Consumption tiers is the way that apps are scaled. Isolated tier apps are hosted in dedicated App Service environments, which are scaled manually. Consumption tier apps are hosted in a shared App Service environment, which is scaled automatically based on demand.

Another difference between the two tiers is the price. Isolated tier apps are more expensive than Consumption tier apps.

**Which tier to choose?**

If you need a high level of security and isolation, or if you need to scale your App Service app manually, then the Isolated tier is the best choice.

If you need a high level of scalability and elasticity, and you don't mind that your App Service app is hosted in a shared environment, then the Consumption tier is the best choice.


The **Isolated tier** has an isolated network in the tiers I explained.

The Isolated tier is a premium tier that offers dedicated hosting, dedicated inbound and outbound IP addresses, and an isolated network. Isolated tier apps are hosted in dedicated App Service environments, which are isolated from other App Service environments and the public internet.

This makes the Isolated tier a good option for high-traffic and mission-critical websites and apps that require a high level of security and isolation. Examples of applications that may need the Isolated tier include:

- Financial applications
- Healthcare applications
- Government applications
- Enterprise applications

If you are unsure whether the Isolated tier is right for your App Service app, you can consult with a Microsoft Azure expert.

