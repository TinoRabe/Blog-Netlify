---
title: 'PowerApps Portals Project Ramp-Up: Provisioning (Licensing)'
date: 2019-11-01T06:00:46.488Z
description: >-
  In this post you will advance your knowledge around considerations for
  choosing the right license for your customers, so you can ramp-up your
  PowerApps Portals project with confidence.
image: /img/license.jpg
---
> tl;dr

**(1)** Recap: PowerApps Portals are licensed differently to Dynamics 365 Portals

**(2)** Recap: PowerApps Portals are licensed via a consumption model (i.e. number of authenticated logins & number of unauthenticated page views)

**(3)** Recap: Dynamics 365 Portals are licensed via an availability level (i.e. number of provisioned instances)

**(4)** Best Practice: Consider leveraging Dynamics 365 Portals for efficient pricing in some scenarios

**(5)** Best Practice: Consider self-hosted Community Portal for evaluation in larger project teams

> Templates - Provisioning of PowerApps Portals

As of the publishing date of this post, there a great differences among the possibilities to license your Portal implementation. As outlined in my previous post ([PowerApps Portal Templates](https://tinorabe.com/post/portals-provisioning-template-licensing-advanced-techniques-to-master-powerapps-portals/)), you are able to provision your portal in a: 

* PowerApps environment **without** Dynamics 365 model-driven apps
* Dynamics 365 model-driven app, i.e. PowerApps environment **with** a Dynamics 365 model-driven apps

In this first post, I have not written about a third option for a new Portal implementation. That is the Community edition of Portals.

The Community edition of Portals is an open-source version of the Portal framework. Historically, Microsoft was kind to publish a certain version (v8.x) of the framework after Adxstudio was aquired and the framework was made available as an add-on appliction to your Dynamics 365 environment. Naturally, the framework for Dynamics 365 Portals has evolved since then, but the Community edition shall not be forgotten in any of your considerations.
