# (table deprecated)
GOOGLE_ANALYTICS_BQ.GA4_APP_INSTALLS

## INTRODUCING NOTE

This table has a list of users who have installed the Patient App at some point.

### TABLE LOGIC

It has all installs recorded in BigQuery, where there has been a user_id assigned to the user (this happens when user logs in) in valid format.


### SOURCE TABLES

`ga-web-us.ga4_mkpl_app.events_raw`

`ga-web-us.ga4_app.install_source`

### CONTACT PERSON

If you have any questions, please contact *Carlo Goes* or Analytics Engineers (Slack: *@analytics engineering*)

## COLUMNS DESCRIPTION

* **user_id**

- `stage_marketplace.user.id` patient user id

* **user_pseudo_id**

- This id is assigned in BigQuery, does not exist in dwh. It is a combination of user + device.

* **country_code**

* **install_date**

- Date that App install was recorded

* **install_source**

- Source of App install (i.e. marketplace banner, Chat, Organic etc.)
