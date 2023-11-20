# google_analytics_bq.investors_kpi

---
### Short description


This table stores basic data about users and sessions collected in Google Analytics 4.

Please note that metrics such as users and sessions has been aggregated for each row separately, meaning that summing them up won't be accurate.


### TABLE LOGIC

This table data is based on GA4's data.

### SOURCE TABLES

- `spectrum.ga4_sessions`

### CONTACT PERSON

If you have any questions, you can contact *Miroslav Tkachenko* or other Analytics Engineers (Slack: *@Miroslav Tkachenko*, *@analytics engineering*)

## COLUMNS DESCRIPTION

* **row_id** - table row unique id.

* **country_code**

* **month** - month and year of the measurement.

* **users** - unique users for this record.

* **sessions** - unique sessions for this record. One user can have multiple sessions in one day.
