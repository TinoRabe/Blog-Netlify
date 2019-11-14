---
title: 'PowerApps Portals Project Ramp-Up: Requirements Gathering'
date: 2019-11-18T18:00:43.148Z
description: >-
  This post will give insights on requirements, which are specific to Power Apps
  Portals. Use this compilation in your requirements gathering process before
  the project starts and during project delivery.
---
> Areas of specific Requirements Gathering

**(1)** Scope

**(2)** User Management

**(3)** Accessibility

**(4)** Best practice: Start with Community Portal template

**(5)** Fit-Gap Analysis

**(6)** Localization

> Scope

![Scope](/img/requirements_scope.jpg "Scope")

The scope of your Power Apps Portals project define what and how requirements will be delivered. It will also give reference on how success is defined and what acceptance means.
The first pillar of a resilient scope management practice is to think about your requirements from a functional point of view. Those requirements are typically formulated together with the business stakeholders. Functional requirements shall describe what value is added to the solution. It could be something like 'As a Portal user, I want to login with my existing Microsoft account so I do not have to remember a separate pair of credentials exclusively to the Portal'.

The technical requirement specification defines how the desired value is realized from a system point of view. Those technical requirements can be documented and tested by test cases separately. In my experience, it is sufficient to make the technical requirement a part of the functional one, e.g. by splitting the user story into a functional and a technical part. So in the example above, the user story is enhanced with a technical spec, e.g. 'External login to be implemented via Azure AD B2C identity provider for all external users (building blocks: Azure AD B2C identity service incl. branding, Portal site settings)'. This will also have the benefit of a documentation on where to look into for troubleshooting of a specific functionality.
- - -

Found this post useful or have comments?\
[Reach out to me anytime.](https://www.linkedin.com/in/tino-rabe-dynamics365/)

> Let's have a closer look at the licensing of Portals in the next blog post - stay tuned.
