---
layout: default
title: Profile CVR
parent: Google Analytics BQ
---

# *GOOGLE_ANALYTICS_BQ.PROFILE_CVR*

## INTRODUCING NOTE

This table stores modelled data about conversion rate of doctors and clinics profiles. Data is available for `web` pageviews (patient app pageviews are not included).

### TABLE LOGIC

The table combines `spectrum.ga4_page_views` data with `spectrum.ga4_sessions` and `spectrum.ga4_bookings` information to provide easy way to calculate CVR for given profile.

CVR calculated with this table is CVR of the single marketplace profile.



### SOURCE TABLES

`spectrum.ga4_page_views`

`spectrum.ga4_sessions`

`spectrum.ga4_bookings`

`stage_marketplace.doctor`

`stage_marketplace.facility`

### CONTACT PERSON

If you have any questions, please contact *Mikołaj Buzała* or other Analytics Engineers (Slack: *@meek*, *@analytics engineering*)

## COLUMNS DESCRIPTION

* **country_code**

* **date**

* **profile_type**

- Type of the profile
  - `Doctor` or `Clinic`

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

* **traffic_source**

- Traffic source data. Value of the `utm_source` link parameter at session's start.

* **traffic_medium**

- Traffic source data. Value of the `utm_medium` link parameter at session's start.

* **traffic_campaign**

- Traffic source data. Value of the `utm_campaign` link parameter at session's start.

* **traffic_content**

- Traffic source data. Value of the `utm_content` link parameter at session's start.

* **traffic_term**

- Traffic source data. Value of the `utm_term` link parameter at session's start.

* **traffic_referrer**

- Traffic referrer


### SESSION CONTEXT

* **landing_page_content_group**

- Content group of the session's landing page

* **is_landing_page**

- Boolean. Whether user landed directly on the profile.


### AGGREGATES

* **sessions**

- Number of sessions with pageview of given profile

* **pageviews**

- Number of pageviews of given profile

* **sessions_with_bookings**

- Number of sessions with booking to given profile (based on EEC context data)
