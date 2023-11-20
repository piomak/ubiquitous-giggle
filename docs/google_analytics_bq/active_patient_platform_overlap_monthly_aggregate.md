---
layout: default
title: Active Patient Platform Overlap Monthly Aggregate
parent: Google Analytics BQ
nav_order: 1
---

# (table deprecated)
active_patient_platform_overlap_monthly_aggregate

## INTRODUCING NOTE

This table stores data about user activity across browsers and devices, based on [user_engagement](https://support.google.com/analytics/answer/11109416) event from GA4.
Data is available from `web` & `app` patients users.


### TABLE LOGIC

The table is monthly aggregation of raw `spectrum.active_patient_platform_overlap`.


### SOURCE TABLES

`spectrum.active_patient_platform_overlap`, which is based on multiple tables in BigQuery


### CONTACT PERSON

If you have any questions, please contact *Miroslav Tkachenko* or other Analytics Engineers (Slack: *@Miroslav Tkachenko *, *@analytics-engineering-team*)

## COLUMNS DESCRIPTION
* **month**


* **country**

  - country_code

* **platform**

  - if platform is app or web

* **user_pseudo_id**

  - GA4's the pseudonymous id (e.g., app instance ID) for the user. In case of web – cookie ID, in case of app – ppp-instance ID.


* **user_id**

  - unique user identifier
