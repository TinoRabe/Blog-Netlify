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

The features of each template are well documented in this [link](https://docs.microsoft.com/en-us/powerapps/maker/portals/portal-templates).

What the documentation does not suggest is some best practices around the provisiosning with t emplate
