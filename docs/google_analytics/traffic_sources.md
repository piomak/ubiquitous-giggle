---
layout: default
title: Traffic Sources
parent: Google Analytics
nav_order: 15
---

# traffic_sources

---
### Short description

This table stores all basic information about traffic sources in the Marketplace collected in Google Analytics.

Data imported from Google Analytics v3 account (Main marketplace account).


---
### Columns

* **traffic_source_id**
Table row unique id.

* **view_id**
Id of Google Analytics view data was taken from, used to join a country to `google_analytics` data. = `google_analytics.view.view_id`.

* **is_sampled**
Boolean. Indicates whether this row was affected by sampling. Sampled data is not 100% accurate. You can read more about sampling here: https://support.google.com/analytics/answer/2637192?hl=en#zippy=%2Ctematy-w-tym-artykule .

* **date**
Date of the measurement.

* **landingcontentgroup1**
Landing group of the session. Indicates type of page - e.g. `Homepage` or `Search Results with Calendars` .

* **source**
Session source. You can read more about source here: https://support.google.com/analytics/answer/6099206?hl=en .

* **medium**
Session medium. You can read more aboutmedium here: https://support.google.com/analytics/answer/6099206?hl=en .

* **campaign**
Sessions campaign. You can read more about campaigns here: https://support.google.com/analytics/answer/6205762?hl=en#zippy=%2Cin-this-article .

* **keyword**
Session keyword. You can read more about keyword here: https://support.google.com/analytics/answer/1033173?hl=en .

* **adcontent**
Session ad content. You can read more about adcontent here: https://support.google.com/analytics/answer/1033173?hl=en .

* **sessions**
Sessions for this record. One users can have multiple sessions in one day.

* **bounces**
Bounces for this record. You can read more about bounce rate here: https://support.google.com/analytics/answer/1009409?hl=en .

* **transactions**
Bookings for this record





---
### Additional notes



---
### Related tables

`google_analytics.view` is necessary proxy to join data from `google_analytics` schema tables with proper country.


---
### Owner/contact person
analytics@docplanner.com / @product_analytics
