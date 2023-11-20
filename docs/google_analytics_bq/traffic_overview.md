# *GOOGLE_ANALYTICS_BQ.TRAFFIC_OVERVIEW*

## INTRODUCING NOTE

This table stores modelled and aggregated data about sessions recorded in GA. Data is available for `web` user bookings (patient app bookings are not included).

### TABLE LOGIC

This table aggregates data from `spectrum.ga4_sessions` table

### SOURCE TABLES

`spectrum.ga4_sessions`


### CONTACT PERSON

If you have any questions, please contact *Mikołaj Buzała* or other Analytics Engineers (Slack: *@meek*, *@analytics engineering*)

## COLUMNS DESCRIPTION

* **country_code**

* **date**
  - Date of the session start

* **device_category**

  - User's device category `mobile`,`tablet` or `desktop`

### LANDING PAGE DATA

* **landing_page**

- URL of the session's landing page

* **landing_page_content_group**

- Content group of the session's landing page

* **landing_profile_doctor_id**

- For sessions that started on the doctor profile = `stage_marketplace.doctor.id`

* **landing_profile_clinic_id**

- For sessions that started on the clinic profile = `stage_marketplace.facility.id`

### TRAFFIC SOURCE DATA

* **traffic_referrer**

  - URL (or domain name) of the page that user was referred to our website.

* **traffic_campaign**

- Traffic source data. Value of the `utm_campaign` link parameter at session's start.

* **traffic_medium**

- Traffic source data. Value of the `utm_medium` link parameter at session's start.

* **traffic_source**

- Traffic source data. Value of the `utm_source` link parameter at session's start.

* **traffic_content**

- Traffic source data. Value of the `utm_content` link parameter at session's start.


### Aggregates

* **sessions**

  - Number of sessions (visits on marketplace)

* **pageviews**

  - Number of pageviews (single pages viewed by users)
