---
layout: default
title: Sessions With Doctor Profile With Calendars
parent: Google Analytics
nav_order: 11
---

# sessions_with_doctor_profile_with_calendars

---
### Short description

This table stores sessions with Doctor Profile with Calendars collected in Google Analytics.
Data imported from Google Analytics v3 account (Main marketplace account).
Number of sessions and users that landed on this page, on this device, from this source on this day. Columns explained below.


---
### Columns

* **sessions_with_doctor_profile_with_calendars_id**
Table row unique id.

* **view_id**
Id of Google Analytics view data was taken from, used to join a country to `google_analytics` data. = `google_analytics.view.view_id`.

* **is_sampled**
Boolean. Indicates whether this row was affected by sampling. Sampled data is not 100% accurate. You can read more about sampling here: https://support.google.com/analytics/answer/2637192?hl=en#zippy=%2Ctematy-w-tym-artykule.

* **segment_id**
Id of segment. Should be joined to `google_analytics.segment.segment_id`.

* **date**
Date of the measurement.

* **devicecategory**
User's device category. Possible values: `mobile`, `desktop` or `tablet`.

* **channelgrouping**
Grouped channel of the sessions. You can read more about channel grouping here https://support.google.com/analytics/answer/6010097?hl=en#zippy=%2Cin-this-article .

* **landingcontentgroup1**
Landing group of the session Indicates type of page - e.g. `Homepage` or `Search Results with Calendars` .

* **campaign**
Sessions campaign. You can read more about campaigns here: https://support.google.com/analytics/answer/6205762?hl=en#zippy=%2Cin-this-article .

* **sourcemedium**
Session source and medium. You can read more about source and medium here: https://support.google.com/analytics/answer/6099206?hl=en .

* **dimension11**
Specialization of the doctor that session contain. Specializations are in local language.

* **users**
Unique users for this record.

* **sessions**
Unique sessions for this record. One users can have multiple sessions in one day.

* **transactions**
Bookings made within the session.



---
### Additional notes

-

---
### Related tables

`google_analytics.view` is necessary proxy to join data from `google_analytics` schema tables with proper country.

`google_analytics.segment` is necessary proxy to join data from `google_analytics` schema tables with proper segment.

---
### Owner/contact person
anna.oppenheim@docplanner.com / @mikolaj.buzala@docplanner.com
