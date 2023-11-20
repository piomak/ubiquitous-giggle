---
layout: default
title: Traffic SM
parent: Google Analytics
nav_order: 14
---

# traffic_sm

---
### Short description

This table stores all basic information about Social Media traffic in the Marketplace collected in Google Analytics.

Data imported from Google Analytics v3 account (Main marketplace account).


---
### Columns

* **traffic_sm_id**
Table row unique id.

* **view_id**
Id of Google Analytics view data was taken from, used to join a country to `google_analytics` data. = `google_analytics.view.view_id`.

* **is_sampled**
Boolean. Indicates whether this row was affected by sampling. Sampled data is not 100% accurate. You can read more about sampling here: https://support.google.com/analytics/answer/2637192?hl=en#zippy=%2Ctematy-w-tym-artykule .

* **segment_id**
Id of segment. Should be joined to `google_analytics.segment.segment_id`.

* **date**
Date of the measurement.

* **landingpagepath**
Landing page of the session.

* **landingcontentgroup1**
Landing group of the session. Indicates type of page - e.g. `Homepage` or `Search Results with Calendars` .

* **sessions**
Unique sessions for this record. One users can have multiple sessions in one day.

* **transactions**
Bookings made within the session.





---
### Additional notes

segment configuration:
      session_from_sm_link_v1: sessions::condition::ga:source==widget;ga:medium=~facebook|instagram|messenger|whatsapp
      session_from_sm_link_v2: sessions::condition::ga:source==widget;ga:keyword=~^facebook|^instagram|^messenger|^whatsapp

---
### Related tables

`google_analytics.view` is necessary proxy to join data from `google_analytics` schema tables with proper country.


---
### Owner/contact person
analytics@docplanner.com / @product_analytics
