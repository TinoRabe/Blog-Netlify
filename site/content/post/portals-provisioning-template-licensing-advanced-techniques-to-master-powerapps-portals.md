---
title: 'PowerApps Portals Project Ramp-Up: Provisioning (Template / Licensing)'
date: 2019-10-28T06:00:19.751Z
description: >-
  In this post you will advance your knowledge around considerations for
  choosing the right template for your customers. You will also find some
  valuable insights for licensing your Portals solution.
image: /img/template.jpg
---
> Templates - Provisioning of PowerApss Portals

As of the publishing date of this post, is it generally possible to leverage pre-built Portals templates with dedicated feature. 
Whenever you wish to applpy such template, it is currently necessary to have at least one qualified Dynamics 365 license (i.e. Dynamics 365 first party model-driven App, such as Sales or Customer Service or Field Service etc.) in your Power Platform tenant ([reference to public documentation](https://docs.microsoft.com/en-us/powerapps/maker/portals/create-dynamics-portal)). This is likely to change in the future, but today that's status quo.

If you do not have such a Dynamics 365 license in your Power Platform tenant, you will not see the templates when creating a new PowerApps Portal. In this case, you will only have the option to create a custom Portals from scratch ('from blank'; ([reference to public documentation](https://docs.microsoft.com/en-us/powerapps/maker/portals/create-portal)).

The following illustration should help you to navigate through your options:

![Overview of Access to Templates for PowerApps Portals](/img/overview_portals-templates.jpg "Overview of Access to Templates for PowerApps Portals")

Let's assume you want to leverage a template, so you may choose from one of the following:

1. Customer Self-Service Portal
2. Partner Portal
3. Employee Self-Service-Portal
4. Community Portal

The features of each template are well documented in this [link](https://docs.microsoft.com/en-us/powerapps/maker/portals/portal-templates). To recap, the choice of template will dictate the schema (i.e. solutions, incl. entities/forms/views/plugin/workflows/etc.) and data (i.e. configuration) that will be installed by Microsoft. What the documentation does not suggest is some best practices around templates.

I found these tips useful in customer facing projects:

* No migration path between templates

Choose your template wisely as there is currently no supported migration path between templates available from Microsoft. There are some undocumented workarounds possible technically, but try to avoid to go down that road whenever possible.

* 80/20 rule: Community Portal

In 80% of the cases, the Community Portal template will do the job and give enough flexibility for future requirements. This template essentially is an extension of the Customer Self-Service template plus useful community features, i.e. blogs and forums. I have been involved in Dynamics 365 Portals projects where the Portal was provisioned with the Customer Self-Service template. After some month and as soon as the users really adopted the Portal, the customer wished to leverage forums, so his user base would be enabled to build communities for troubleshooting on their own in forums. 

If you can be certain to never use the community features and only need customer service functionalities, the Customer Self-Service template may be your way to go. Always keep in mind that pages can be hidden and maybe exposed again at a later point in time.

* 
