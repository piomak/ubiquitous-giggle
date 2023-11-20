---
layout: default
title: GA4 Marketing Pageviews
parent: Google Analytics BQ
---

# *google_analytics_bq.ga4_marketing_pageviews*

## INTRODUCING NOTE

This table stores data about all page views on our website in the Pro area.

### TABLE LOGIC

The table pulls the only the Page view event from the table containing raw data for all countries and dates: "ga-web-us.ga4_marketing.events_raw"

### SOURCE TABLES

"ga-web-us.ga4_marketing.events_raw"
"ga-web-us.config.timezone"

### CONTACT PERSON

If you have any questions, please contact *Kate Baranova*

## COLUMNS DESCRIPTION

* **event_name**

* **country_code**

* **date**

- Date of the page view event in format "YYYY-MM-DD"

* **unified_session_id**

* **doctor_id**

-  Doctor Id in case user_id follows the pattern doctor-******

* **facility_id**

- Facility Id in case user_id follows the pattern facility-******

* **user_id**

- ID available for some Doctors/Facilities if they browse while logged in
* **user_pseudo_id**

- Unique ID for all users who browse the website


### PAGEVIEW DATA

* **pageview_id**

- Unique ID of each Page View event

* **pageview_timestamp**

- Timestamp for each pageview even

* **page_location**

- Link of the page viewed. Cleaned and easily readable


* **page_title**

- Title of the page viewed


* **source**

- Traffic source data. Value of the `utm_source` link parameter at session's start.


* **campaign**

- Traffic source data. Value of the `utm_campaign` link parameter at session's start..

* **medium**

- Traffic source data. Value of the `utm_medium` link parameter at session's start.

* **engagement_msec**

- The engagement time for each page view event. Can be 0 as well

* **first_session**

- Conditional field to identify user´s first session based on pageview timestamp. Boolean values
