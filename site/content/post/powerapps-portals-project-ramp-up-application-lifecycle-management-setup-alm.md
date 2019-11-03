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

> Preamble

This is my personal take on a resilient ALM setup strategy. Still, there are many opinions about this out there, so hopefully you can take some benefits out of it for your personal ALM setup strategy. This post will not discuss about the technical setup of an ALM setup. Please look at it from a strategic point of view and than choose your favourite tools and system setups to support that strategy.

> ALM Setup - Introduction

In my years as a functional consultant, I have come worked in projects of different scale:

* Enterprise Business
* Small-Medium sized Business
* One Man Business

Almost in every project, the ALM setup strategy led to some discussion in the beginning of the project. In their essence, these discussions and considerations are not particularly unique to PowerApps Portals projects, but rather to software delivery projects in general. Still, I always bring this topic up in the very beginning of the project and too often the ALM setup strategy has not been considered deep enough by the customer. Hence, I feel this is a crucial factor to a healthy project. This is my personal opinion among many opinions out there. Microsoft has just released a [guidance for efficient environment setup strategies on the PowerPlatform](https://powerapps.microsoft.com/en-us/blog/establishing-an-environment-strategy-for-microsoft-power-platform/) themselves - give it a read and maybe find a model in between that works best for your project. Let's start with projects at enterprise scale. Here's a sample illustration, which should not be anything new to you:

![ALM setup Enterprise](/img/alm-enterprise.jpg "ALM setup Enterprise")

Now let's deep dive into each pillar of the setup:

1. **Sandbox:** Use a dedicated sandbox instance to explore the framework features **for yourself being the ISV**. Not only explore them, but test them until you break them (from a technical or from a requirements perspective). Use such sandbox to build confidence and become an expert for certain areas/features of the framework. A dedicated sandbox is also great to conduct proof of concepts (PoCs) before delivering requirements in the DEV environment. At any point consider to push a customizations or even a copy from your DEV environment to Sadbox, to have a more realistic base for your PoCs.

2. **DEV**: Typically, this is where the requirements are delivered. Once a requirement is delivered, a unit test along some regression testing shall be executed by the implementing team in this environment.

3. **TEST**: Deploy your customization and let another testing party (e.g. your dedicated internal test team) perform the same unit tests along some regression testing. Maybe your project requires some integration with 3rd party systems- that is a great environment to test those integrations and to learn by the progress you are making, so the final integration with productive data can run as smoothly as possible. 

4. **QA (Quality Assurance)**: Analogous to TEST, delivered requirements will be tested here. In contrast though, the customer will be the testing party this time. Invite relevant testing stakeholders to this environment and gather their feedback. Examples: Functional requirements, such as features or user experiences, can be tested by the business. Critical security mechanisms and features can be tested by the IT. Consider QA to deliver training to your customer and maybe let the customer train their user base by themselves in QA.
