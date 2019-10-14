---
title: >-
  Lessons Learned #1 - Cannot find newly created product records in Field
  Service Mobile App
date: 2019-08-30T20:27:55.837Z
description: >-
  An approach to automatically activate all new product records when created
  form the Field Service Mobile App
image: /img/david-kovalenko-g85vutpw6jg-unsplash.jpg
---
# **Problem**

I observed that an OOTB Field Service solution (incl. the Mobile App) lets the user create a new product record. But this record does not directly appear in any of the product lookup fields within the App. The root cause of this behavior is that as per the Dynamics 365 Customer Engagement standard, all new products are created in draft state. Hence, only published products are visible in the standard Field Service Mobile App project.



# **Solution**

The easiest approach could be a system setting in Dynamics 365, which will create all new product records in published state rather than in draft state (refer to Microsoft documentation). If the option is toggled to 'Yes' then all new product records will be published directly and therefore will appear in any of the product lookup fields of the Field Service Mobile App.



# **Addendum**



This is one of many approaches to the problem and easy to realize. If your organization and solution architecture permits, it can be an easy fix.

Be careful though to give each individual Field service Mobile App user the possibility to extend the product catalog directly from within the app.

As always, it needs to be analyzed for applicability in the specific use case.
