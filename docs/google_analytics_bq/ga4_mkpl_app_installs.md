---
layout: default
title: GA4 MKPL App Installs
parent: Google Analytics BQ
---

GOOGLE_ANALYTICS_BQ.GA4_MKPL_APP_INSTALLS

## INTRODUCING NOTE

This table aggregates patient app installs by date & source.

### TABLE LOGIC

It has all installs recorded in BigQuery.


### SOURCE TABLES

`ga-web-us.ga4_mkpl_app.events_raw`

### CONTACT PERSON

If you have any questions, please contact *Carlo Goes* or Analytics Engineers (Slack: *@analytics engineering*)

## COLUMNS DESCRIPTION

* **country_code**

* **date**


Date that App install was recorded

* **operating_system**

User's operating system: `Android` or `iOS`

* **install_source**

Source of App install (i.e. marketplace banner, Chat, Organic etc.)

* **installs**

Number of installs
