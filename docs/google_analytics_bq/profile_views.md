---
layout: default
title: Profile Views
parent: Google Analytics BQ
---

# *GOOGLE_ANALYTICS_BQ.PROFILE VIEWS*

## INTRODUCING NOTE

This table stores modelled data about pageviews of doctors and clinics profiles, search activity before the PV and traffic source details. Data is available for `web` pageviews (patient app pageviews are not included).

### TABLE LOGIC

The table enhances `spectrum.ga4_page_views` data with `spectrum.ga4_sessions` information. If there is no GA data available for given booking, it is not included in this table.


### SOURCE TABLES

`spectrum.ga4_page_views`

`spectrum.ga4_sessions`

`stage_marketplace.doctor`

`stage_marketplace.facility`

### CONTACT PERSON

If you have any questions, please contact *Mikołaj Buzała* or other Analytics Engineers (Slack: *@meek*, *@analytics engineering*)

## COLUMNS DESCRIPTION

* **country_code**

* **date**

* **profile_type**

- Type of the profile
  - `doctor` or `clinic`

* **mkpl_doctor_id**

- `stage_marketplace.doctor.id` profile doctor id, not null for `profile_type = 'doctor'`

* **mkpl_clinic_id**

- `stage_marketplace.facility.id` profile clinic id, not null for `profile_type = 'clinic'`

* **content_group**

- Content group of the profile - differentiating calendar/non calendar and premium/basic profiles.

* **profile_url**

- Profile URL

* **device_category**

- User's device category = `mobile` / `desktop` / `tablet`

### TRAFFIC DATA

* **traffic_campaign**

- Traffic source data. Value of the `utm_campaign` link parameter at session's start.


* **traffic_medium**

- Traffic source data. Value of the `utm_medium` link parameter at session's start.


* **traffic_source**

- Traffic source data. Value of the `utm_source` link parameter at session's start.


* **traffic_content**

- Traffic source data. Value of the `utm_content` link parameter at session's start.

* **traffic_term**

- Traffic source data. Value of the `utm_term` link parameter at session's start.

* **traffic_referrer**

- Traffic referrer


### SESSION CONTEXT

* **is_landing_page**

- Boolean. Whether user landed directly on the profile.

* **landing_page_content_group**

- Content group of the session's landing page

* **previous_page_content_group**

- Content group of the session's previous page

* **specialization_context**

- Last searched specialization before entering the profile. = `stage_marketplace.specialization.id`

* **eec_list_name**

- Last search click's list name (list of search parameters)

### AGGREGATES

* **views**

- Number of pageviews
