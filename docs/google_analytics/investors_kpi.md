---
layout: default
title: Investors KPI
parent: Google Analytics
nav_order: 6
---

# investors_kpi

**Please note that there is a new version of investors_kpi table, you can find it at `google_analytics_bq.investors_kpi`.**

---
### Short description

This table stores basic data about users and sessions collected in Google Analytics.
Used for investors KPI. More info @adam.krystian@docplanner.com .


---
### Columns

* **investors_kpi_id**
Table row unique id.

* **view_id**
Id of Google Analytics view data was taken from, used to join a country to `google_analytics` data. = `google_analytics.view.view_id`.

* **is_sampled**
Boolean. Indicates whether this row was affected by sampling. Sampled data is not 100% accurate. You can read more about sampling here: https://support.google.com/analytics/answer/2637192?hl=en#zippy=%2Ctematy-w-tym-artykule.

* **segment_id**
Id of segment. Should be joined to `google_analytics.segment.segment_id`.

* **yearmonth**
Month and year of the measurement.

* **users**
Unique users for this record.

* **sessions**
Unique sessions for this record. One users can have multiple sessions in one day.



---
### Additional notes

-

---
### Related tables

`google_analytics.view` is necessary proxy to join data from `google_analytics` schema tables with proper country.


---
### Owner/contact person
anna.oppenheim@docplanner.com / @mikolaj.buzala@docplanner.com / @adam.krystian@docplanner.com
