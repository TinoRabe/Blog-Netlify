---
title: 'PowerApps Portals Project Ramp-Up: Project Management'
date: 2019-11-11T19:00:00.000Z
description: >-
  Power Apps Portals projects have their specifics when it comes to project
  management. Read this blog post and learn from my best practices that shall be
  considered to run a robust project management practice.  
image: /img/project-management.jpg
---
> tl:dr

**(1)** When choosing the project management tool chain, consider enablement of collaboration within your Portals team and outside your team with other project teams. There will always be an intersection.

**(2)** Consider ways to document your Portals configuration, so they can be traced back - both functionally and technically.

**(3)** Create your test data in advance and let it be reproducible in every environment.

**(4)** When running an agile project, consider the ability to independently deploy anytime.

**(5)** Train involved project staff about Power Apps Portals right form the beginning as this will reduce time and efforts during project delivery.

**(6)** Do not underestimate efforts for the transition to operations after a the project ends.

![](/img/portals-project-management.jpg)

Now let's deep dive into depicted specifics of project management in Power Apps Portals projects.

> Methodology

Every project shall follow some sort of defined methodology; may it be the one of your choice. When comparing those methodologies, consider your way to an efficient collaboration model. Most likely, your Portals project will be accompanied by other projects, e.g. for development of the core application that your customer will use to do business. Often the Portals project is much smaller than the core project in terms of staff and budget. Still, your Portals project is equally important as this is probably the forefront for the customers of your customer, i.e. the people, your customer drives business with. So choose your collaboration model wisely as there will be joint efforts, such as business process design or changes to CDS schema. If those project teams are not regularly synchronized, the project will not as smoothly as required. In my projects, it has proven to be efficient to have at least one functional consultant in each of the separate project teams. Those consultants inform and dispute about requirements of every team and eventually conclude to a consensus that drives a more effective solution. As a side benefit, knowledge is shared across project teams and unavailability of team members can be covered to a certain extent. 

Once your collaboration model has been selected, do your research on the most effective yet easy tool chain for your collaboration processes. Azure DevOps Services from Microsoft deliver great value in project teams of small and large scale. It is important to enable each project member right from the beginning to be able to find, complete & document their work items. Another key area to be covered is an intuitive way to collaborate on work items within your Portals project and outside with other project teams. Think about how to document test cases and how to  track the execution of those.



> Requirements

Traceability of requirements, decisions and solution components is key to a robust project management. At any point of time, may it be during or after the project delivery, you must be able  to recall those work items artifacts. I favor to leverage the concept of user stories for functional and technical requirements documentation. The functional part of the user story will be formulated by the businesses and describes the expected outcome to achieve an anticipated value. In that same user story, I always note down the technical side of how the outcome is achieved. That could be the name of a configuration artifact (e.g. Web Page, Entity Form Metadata or piece of JavaScript) or the required CDS schema (e.g. form, view or flow). On that same user story, important decisions are being noted down, too. Being able to track back when and why this artifact was put into place can be a huge time saver and quickly answers endless discussions at a a later point in time - potentially to people, who will join the project later.
