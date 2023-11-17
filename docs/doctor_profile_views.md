# doctor_profile_views

---
### Short description

This table stores all basic information about doctor profile views. It's used to provide statistics on doctor profile

Data imported from Google Analytics v3 account (Main marketplace account).


---
### Columns

* **doctor_profile_views_id**
Table row unique id.

* **view_id**
Id of Google Analytics view data was taken from, used to join a country to `google_analytics` data. = `google_analytics.view.view_id`.

* **is_sampled**
Boolean. Indicates whether this row was affected by sampling. Sampled data is not 100% accurate. You can read more about sampling here: https://support.google.com/analytics/answer/2637192?hl=en#zippy=%2Ctematy-w-tym-artykule .

* **date**
Date of the measurement.

* **dimension20**
Doctor profile id = `stage_marketplace.doctor.id`. Stored as varchar due to GA data model, needs to be converted to number before any join.

* **pageviews**
Number of total views of the profile.

* **uniquepageviews**
Unique views for this record. One user can have multiple views of the same doctor profile during one session.

* **entrances**
Number of sessions that started on the profile.





---
### Additional notes

---
### Related tables

`google_analytics.view` is necessary proxy to join data from `google_analytics` schema tables with proper country.
`staeg_marketplace.doctor`

---
### Owner/contact person
analytics@docplanner.com / @product_analytics
