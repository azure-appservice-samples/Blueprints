---
layout: default
description: "A quick brown fox jumps over the lazy dog"
---

# How App Service Works

+ [What is App Service?](#what-is-app-service)
   + [Web App](#web-app)
   + [Mobile App](#mobile-app)
   + [API App](#api-app)
   + [Logic App](#logic-app)
+ [Understanding App Service Plans](#understanding-app-service-plans)
+ [App Service Architecture Overview](#app-service-architecture-overview)
+ [Introduction to App Service Environment](#introduction-to-app-service-environment)
+ [Azure App Service Development Stack Support](azure-app-service-development-stack-support)
   + [Classic ASP](#classic-asp)
   + [ASP.NET](#asp-net)
   + [PHP](#php)
   + [Node.js](#node-js)
   + [Java](#java)
   + [Python](#python)

## What is App Service?

Azure App Service is the only cloud service that integrates everything you need to quickly and easily build web and mobile apps for any platform and any device. Built for developers, App Service is a fully managed platform with powerful capabilities such as built-in DevOps, continuous integration with Visual Studio Online and GitHub, staging and production support, and automatic patching.

### Web App

[Azure App Service Web Apps](https://azure.microsoft.com/en-us/documentation/articles/app-service-web-overview/) is a fully managed platform that enables you to build, deploy and scale enterprise-grade web apps in seconds. Focus on your application code, and let Azure take care of the infrastructure to scale and securely run it for you. Web Apps is:

+ **Familiar and Fast** - Use your existing skills to code in your favorite language, framework, and IDE. With just a few clicks, add versioning, updating, single sign-on, identity broker, isolated storage, and performance monitoring to your existing web apps. Access a rich gallery to use as building blocks to accelerate your development. Experience unparalleled developer productivity with cutting edge capabilities like continuous integration, live-site debugging, and industry leading Visual Studio IDE.

+ **Enterprise Grade** - Web Apps is designed for building and hosting secure mission-critical applications. Build Active Directory integrated business apps that connect securely to on-premises resources, then host them on a secure cloud platform that is ISO, SOC2, and PCI compliant. All while enjoying enterprise level SLAs.

+ **Global Scale** - Web Apps is optimized to provide availability and automatic scale on a global datacenter infrastructure. Easily scale applications up or down on demand. With high availability provided within and across different geographical regions. Replicating data and hosting services in multiple locations is quick and easy, making expansion into new regions and geographies as simple as a mouse click.

### Mobile App

[Mobile Apps in Azure App Service](https://azure.microsoft.com/en-us/documentation/articles/app-service-mobile-value-prop-preview/) offers a highly scalable, globally available mobile application development platform for Enterprise Developers and System Integrators that brings a rich set of capabilities to mobile developers. With Mobile Apps you can:

+ **Build native and cross platform apps** - whether you're building native iOS, Android, and Windows apps or cross-platform Xamarin or Cordova (Phonegap) apps, you can take advantage of App Service using native SDKs.

+ **Connect to your enterprise systems** - with Mobile Apps you can add corporate sign on in minutes, and connect to your enterprise on-premises or cloud resources.

+ **Connect to SaaS APIs easily** - with more than 40 SaaS API connectors, you can easily integrate your app with SaaS APIs your enterprise uses today. Want to update account status in both CRM and the billing system? Mobile Apps offer enterprise SaaS APIs at your fingertips.

+ **Build offline-ready apps with sync** - make your mobile workforce productive by building apps that work offline and use Mobile Apps to sync data in the background when connectivity is present with any of your enterprise data sources or SaaS APIs.

+ **Push Notifications to millions in seconds** - engage your customers with instant push notifications on any device, personalized to their needs, sent when the time is right.

### API App

[Azure App Service API Apps](https://azure.microsoft.com/en-us/documentation/articles/app-service-api-apps-why-best-platform/) provides capabilities for developing, deploying, publishing, consuming and managing RESTful web APIs. App Service provides the following features available today in public preview:

+ **Easy consumption** - Integrated Swagger support makes your APIs easily consumable by a variety of clients. The API Apps SDK can generate client code for your APIs in a variety of languages including C#, Java, and Javascript.

+ **Simple access control** - Built-in authentication services support Azure Active Directory or third-party services such as Facebook and Twitter. You can protect an API app from unauthenticated access with no changes to your code. If you're familiar with the authentication services provided by Azure Mobile Services, API Apps builds on that framework and extends it to APIs hosted by API Apps. The App Service SDK also enables you to use a simplified syntax for authorization code. For more information, see Authentication for API apps and mobile apps in Azure App Service.

+ **Easy connection to SaaS platforms** - Connector API apps in the Azure Marketplace are provided by Microsoft and third parties to simplify the code you write for interacting with SalesForce, Office 365, Twitter, Facebook, Dropbox, and many others.

+ **Integration with Logic Apps** - API apps that you create can be consumed by App Service Logic Apps. 

+ **Visual Studio integration** - Dedicated tools in Visual Studio streamline the work of creating, deploying, debugging, and managing API apps.

### Logic App

[Azure App Service Logic Apps](https://azure.microsoft.com/en-us/documentation/articles/app-service-logic-what-are-logic-apps/) allow developers to design workflows that start from a trigger and then execute a series of steps, each invoking an App Service API app whilst securely taking care of authentication and best practices like checkpointing and durable execution.

If you want to automate any business process (e.g. find negative tweets and post to your internal slack channel or replicate new customer records from SQL, as they arrive, into your CRM system) Logic Apps makes integrating disparate data sources, from cloud to on-premises easy. Check out our connectors for more inspiration and get started now to see what you can do. 

What's more, with our BizTalk API Apps you can scale to mature integration scenarios with the power of a rules engine, trader partner management and more.

+ **Easy to use design tools** - Logic Apps can be designed end-to-end in the browser. Start with a trigger - from a simple schedule to whenever a tweet appears about your company. Then orchestrate any number of actions using the rich gallery of connectors.

+ **Compose SaaS easily** - Even composition tasks that are easy to describe are difficult to implement in code. Logic Apps make it a cinch to connect disparate systems. Want to create a task in your CRM software that is based on the activity from your Facebook or Twitter accounts? Want to connect your cloud marketing solution to your on-premises billing system? Logic apps are the fastest, most reliable way to deliver solutions to these problems.

+ **Get started quickly from templates** - To help you get started we've provided a gallery of templates that allow you to rapidly create some common solutions. From advanced BizTalk solutions to simple SaaS connectivity, and even a few that are just 'for fun' - the gallery is the fastest way to understand the power of Logic Apps.

+ **Extensibility baked in** - Don't see the connector you need? Logic Apps are part of the App Service suite and designed to work with API apps; you can easily create your own API app to use as a connector. Build a new app just for you, or share and monetize in the marketplace.

+ **Real integration horsepower** - Start easy and grow as you need. Logic Apps can easily leverage the power of BizTalk, Microsoft's industry leading integration solution to enable integration professionals to build the solutions they need. Find out more about the BizTalk capabilities provided with App Services.

## Understanding App Service Plans

An [App Service plan](https://azure.microsoft.com/en-us/documentation/articles/azure-web-sites-web-hosting-plans-in-depth-overview/) represents a set of features and capacity that you can share across multiple apps in Azure App Service, including Web Apps, Mobile Apps, Logic Apps or API Apps. These plans support 5 pricing tiers (Free, Shared, Basic, Standard and Premium) where each tier has its own capabilities and capacity. Apps in the same subscription and geographic location can share a plan. All the apps sharing a plan can leverage all the capabilities and features defined by the plan's tier. All apps associated with a given plan run on the resources defined by the plan. For example, if your plan is configured to use two "small" instances in the standard service tier, all apps associated with that plan will run on both instances and will have access to the standard service tier functionality. Plan instances on which apps are running on are fully managed and highly available.

## App Service Architecture Overview



## Introduction to App Service Environment

An [App Service Environment](https://azure.microsoft.com/en-us/documentation/articles/app-service-app-service-environment-intro/) is a Premium service plan option of Azure App Service that provides a fully isolated and dedicated environment for securely running Azure App Service apps at high scale, including Web Apps, Mobile Apps, and API Apps. 

App Service Environments are ideal for application workloads requiring:

+ Very high scale
+ Isolation and secure network access

App Service Environments are isolated to running only a single customer's applications, and are always deployed into a virtual network. Customers have fine-grained control over both inbound and outbound application network traffic, and applications can establish high-speed secure connections over virtual networks to on-premises corporate resources.

## Azure App Service Development Stacks Support

The Azure App Service team passionately invests in a support model for [development stacks](https://azure.microsoft.com/en-us/blog/windows-azure-websites-development-stacks-support/) that allows your web apps to start running quickly and gives your web apps room to grow. There are a few basic principles we use for versioning and extensibility of development stacks and how these principles apply to your web apps. 

Some development stacks we support such as PHP are designed to enable side by side versions. For these development stacks we provide a set of current versions that have been validated for our platform. We also establish a default so no input is required unless you prefer a specific version for compatibility reasons.

Other development stacks such as .NET are designed to provide in-place upgrade of some versions (e.g. .NET 4.5). In this case we work hard to maintain a current view of the development stack and provide you with the features and benefits of the latest versions.

### Classic ASP  
### ASP.NET  
### PHP  
### Node.js  
### Java  
### Python  
