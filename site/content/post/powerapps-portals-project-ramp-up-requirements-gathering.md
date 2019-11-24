---
title: 'PowerApps Portals Project Ramp-Up: Requirements Gathering (Scope)'
date: 2019-11-24T18:00:43.148Z
description: >-
  This post will give insights on requirements, which are specific to Power Apps
  Portals. Use this compilation of best practices in your requirements gathering
  process before the project starts and during project delivery.
---
> Areas of specific Requirements Gathering

**(1)** Scope

**(2)** User Management

**(3)** Accessibility

**(4)** Fit-Gap Analysis

**(5)** Localization

> Scope 
> ![Scope](/img/requirements_scope.jpg "Scope")

**Functional:**\
The scope of your Power Apps Portals project defines what and how requirements will be delivered. It will also give reference on how success is defined and what acceptance means.
The first pillar of a resilient scope management practice is to think about your requirements from a functional point of view. Those requirements are typically formulated together with the business stakeholders. Functional requirements shall describe what value is added to the solution. It could be something like 'As a Portal user, I want to login with my existing Microsoft account so I do not have to remember a separate pair of credentials exclusively to the Portal'.

**Technical:**\
The technical requirement specification defines how the desired value is realized from a system point of view. Those technical requirements can be documented and tested by test cases separately. In my experience, it is sufficient to make the technical requirement a part of the functional one, e.g. by splitting the user story into a functional and a technical part. So in the example above, the user story is enhanced with a technical spec, e.g. 'External login to be implemented via Azure AD B2C identity provider for all external users (building blocks: Azure AD B2C identity service incl. branding, Portal site settings)'. This will also have the benefit of a documentation on where to look into for troubleshooting of a specific functionality.

**Targets:**\
Consider targets as the motivation or the guidance in your functional requirements specification. Those shall describe the ROI (Return of Investment) and why this is relevant to the solution. Adding this to our exemplary user story could be something like: 'Leveraging an existing Microsoft account as primary login improves usability and reduces administration/training efforts in comparison to local login'.

**Non-Targets:**\
The non-targets shall not describe the negation of the formulated target, but rather the limits of the targets. It will help the reader to further understand the core of the target. A non-target could also describe the conditions to not meet the ROI. Take this example in our user story: 'Leveraging identity providers other than Microsoft is not required as 90% of our users have a Microsoft account'.

This is what our exemplary user story could look like by now:

![User Story](/img/requirements_userstory.jpg "User Story")

**Acceptance Criteria:** \
An acceptance criteria is usually formulated within the test case. It describes the expected result out of a defined action. Consider this to be a crucial point in your requirements gathering process as it will define how your solution artifacts are accepted by the customer. From customer side, they can be used to describe the critical conditions under a functionality is considered to be functional at its core. An example test case for our user story could be:

![Test Case](/img/requirements_testcase.jpg "Test Case")

 **Quality Gates:** \
This certainly is not a must have, but best practice. A quality gate defines the availability of a critical building block of your solution, especially as it can have a dependency to subsequent building blocks. In our example this could be 'External authentication working and tested as expected'.

> User Management
> ![](/img/requirements_user-management.jpg)

** User-In** \
A crucial aspect to an effective solution for the Portal users ist the user-in process. This will likely be the first touch point and therefore the first impression those users will have. From my experience, the customer has a clear picture of which functionality the Portal has to cover. But the user experience from 'click one' is ever so often neglected. This becomes especially true if the Portal aims to be a self-service Portal. Consider the following questions for your requirements gathering:

* Which method of user registration shall be realized (self registration, prepared invitation, requested invitation, provisioning of credentials upfront, registration via federation with external identity providers)?
* How will relevant Web Roles be applied (manually, automatically)?
* What happens after the first successful login, e.g. to which web page will the user directed and which information is exposed/demanded?
* Is it useful to send a follow up email separately after the first login (e.g. suggest guidance via documentation/help area/demo/videos/etc.)?
* Who and when shall monitor the completion of open invitations?
* What is the threshold of failed login attempts and what are the next steps, maybe even automated?

** User-Out** \
Another area to pay attention to are requirements to the user-out process. This time it is not so much about user experience, but rather important to the management of data quality and integrity.
Here are some questions for guidance:

* Shall it be possible to open the possibility to request an user account deactivation/deletion?
* If an user account is no longer active, what shall happen with assigned records (e.g.open cases or open activities)?
* Who and when shall monitor user accounts that have not logged in for a defined periods of time, e.g. have not logged in for more than 12 months)?
* Is it necessary to leverage the functionality to have users locked out after a certain attempt of failed logins?

** User Management** \
The last area in user management that I would like to share my best practices on is the user support. A first class user support can be a game changer and drive user adoption massively. Imagine a self service portal, which is designed to be intuitive, but leaves the majority of users puzzled for some of the core functionalities. Or that they regularly experience bugs/malfunctions in their everyday usage. Hence, here are some questions to drive the requirements gathering:

* How and where shall the user be able to report bugs/malfunctions? 
* What does the user experience in the resolution/feedback process look like?
* Where and how does the user request for help within the Portal?
* Can it be useful to leverage the forums area to enable user to help each other?
* Can it be useful to expose some of the knowledge articles just for Portal usage topics?
* Can a virtual agent be leveraged to reduce support efforts?
* How is the effectiveness of the Portal evaluated?

> Accessibility
> ![Accessibility](/img/requirements_accessibility.jpg "Accessibility")

During the requirements gathering process, it will be useful to put yourself in the shoes of the Portal users. Know your Portal users and tailor your Portal solution specifically to create an effective solution and drive user adoption. 

 **Service Consumption** \
Take this as a bad example for misconceived consumption of a Portal solution:
The Portal gives rich information via entity lists with useful filtering and searching. Unfortunately, the exposed  lists have more than 20 columns and the majority of users (at least 80%) use the Portal from a mobile browser on their smartphone. Now such wide entity lists can easily become unusable or the filter area becomes to big. Another example are pictures, which are optimized for the desktop client, but do not scale down well enough when accessed on a mobile device. 

 **Color Scheme** \
Another area of great accessibility is an acceptable color scheme. Maybe the customer requests the adherence to some corporate identity color scheme, which makes content hard to read. Also consider your requirements gathering in terms of color scheme for a guided user experience as well. Have important information to show? Make it standout from the not-so-important information by applying a meaningful colors that will not mislead the Portal user and captures user attention usefully. Also consider font style and font size to present content to the audience in an appropriate manner.

 **JavaScript: Browser Support** \
It can be best practice to define the set of browsers you aim to support with your solution. You do not want to run critical business logic on web pages with custom client-side scripts, which are not being executed by the browsers of your user base. Consider your user base and maybe state supported browsers in a dedicated Portals FAQ, so users are not left frustrated through unnecessary intransparency. Another way to overcome this shortcoming would be a well-designed JavaScript solution, which informs the user as soon as incompatibility is detected (e.g. dedicated alerts or remarks). In a later post, I will share some best practice on how to monitor the Portal service health towards detected browser exceptions on client-side by leveraging Azure Application Insights.

> Fit-Gap Analysis
> ![Fit-Gap Analysis](/img/requirements_fitgap.jpg "Fit-Gap Analysis")

So let's look at some best practices on how to identify requirements and considerations on how to document them. 

** Portals Standard vs. Requirements ** \
You're up to a good start if you know the Portal functionality very well. And this is template specific, if a template is used. If you leverage the customer self-service template, deep-dive into the template specific Web templates of the solution. If you know all the templates and their unique features, it will be a lot easier to not only choose the right template for your customer needs, but also shape your solution architecturally with out-of-the-box features. Consider to categorize the gathered requirements into at least three categories:
* Standard functionality without customization
* Standard functionality with customization
* Custom functionality

This can make life easier when it comes to comprehend estimated efforts and also maintains a first class documentation of your solution. Put yourself in the shoes of the support staff after the project phase. Wouldn't it be nice to know straight away that a buggy feature is relying on standard functionality? That will make troubleshooting so much easier as reproduction in other (vanilla) environments can be carried out right away.

 - - -

Found this post useful or have comments?\
[Reach out to me anytime.](https://www.linkedin.com/in/tino-rabe-dynamics365/)

> Let's have a closer look at the licensing of Portals in the next blog post - stay tuned.
