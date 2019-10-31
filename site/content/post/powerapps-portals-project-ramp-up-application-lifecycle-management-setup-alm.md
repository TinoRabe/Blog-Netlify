---
title: >-
  PowerApps Portals Project Ramp-Up: Application Lifecycle Management Setup
  (ALM)
date: 2019-11-04T07:00:49.337Z
description: >-
  Learn how to structure your environment in dependency of the Portals project
  type. I will share best practices that I have come across based on actual
  experience from customer-facing Portals projects. This post will give pros and
  cons for individual ALM setup strategies. Build knowledge to reflect, consult
  and decide on the ALM setup today to drive a professional Portals projects.
image: /img/alm.jpg
---
> tl;dr

**(1)** Best Practice: Scale ALM setup in dependency to project scale (e.g. enterprise project, small-medium sized project, etc.)

**(2)** Best Practice: Consider at least two groups of stakeholders: You and your customer

**(3)** Best practice: Try to avoid a single-portal approach

**(4)** Best practice: Have your ALM setup strategy in place before the actual requirements delivery starts

> ALM Setup - Introduction

In my years as a functional consultant, I have come worked in projects of different scale:

* Enterprise Business
* Small-Medium sized Business
* One Man Business

Almost in every project, the ALM setup strategy led to some discussion in the beginning of the project. In their essence, these discussions and considerations are not particularly unique to PowerApps Portals projects, but rather to software delivery projects in general. Still, I always bring this topic up in the very beginning of the project and too often the ALM setup strategy has not been considered deep enough by the customer. Hence, I feel this is a crucial factor to a healthy project. Let's start with projects at enterprise scale. Here's a sample illustration, which should not be anything new to you:

![ALM setup Enterprise](/img/alm-enterprise.jpg "ALM setup Enterprise")

Now let's deep dive into each pillar of the setup:

1. **Sandbox:** Use a dedicated sandbox instance to explore the framework features **for yourself being the ISV**. Not only explore them, but test them until you break them (from a technical or from a requirements perspective). Use such sandbox to build confidence and become an expert for certain areas/features of the framework. A dedicated sandbox is also great to conduct proof of concepts (PoCs) before delivering requirements in the DEV environment.

2. **DEV**: Typically, this is where the requirements are delivered. Once a requirement is delivered, a first unit test along some regression testing shall not be forgotten in this environment.

3. TEST: Deploy you customizations and perform another unit test along some regression testing
