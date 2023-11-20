---
layout: default
title: GA4 MKPL App Sessions
parent: Google Analytics BQ
---

GOOGLE_ANALYTICS_BQ.GA4_MKPL_APP_SESSIONS

## INTRODUCING NOTE

This table presents all sessions recorded in patient app in granular form.

### TABLE LOGIC

It has all sessions recorded in BigQuery.


### SOURCE TABLES

`ga-web-us.ga4_mkpl_app.events_raw`

### CONTACT PERSON

If you have any questions, please contact *Carlo Goes* or Analytics Engineers (Slack: *@analytics engineering*)

## COLUMNS DESCRIPTION

* **country_code**

* **date**

* **unified_session_id**

GA session ID unique across all countries.

* **user_pseudo_id**

User's Pseudo ID. Roughly translates to one device that app is installed on. Unique for one country.

* **device_category**

Whether `mobile` or `tablet`.

* **operating_system**

User's operating system: `Android` or `iOS`

* **landing_screen**

First application screen displayed in a session.

* **landing_screen_class**

Class of the first application screen displayed in a session.

* **screens_visited**

Number of application screens visited in a session.
