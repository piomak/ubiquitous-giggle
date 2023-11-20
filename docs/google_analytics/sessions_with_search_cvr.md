---
layout: default
title: Sessions with search CVR
parent: Google Analytics
nav_order: 12
---

# Sessions with search CVR

---
### Short description

This table stores sessions with Search visited collected in Google Analytics.
Data imported from Google Analytics v3 account (Main marketplace account).
Number of sessions and users that landed on this page, on this device, from this source on this day. Columns explained below.


---
### Columns

* **sessions_with_search_id** <br>
Table row unique id.


* **view_id** <br>
Id of Google Analytics view data was taken from, used to join a country to `google_analytics` data. = `google_analytics.view.view_id`.


* **is_sampled** <br>
Boolean. Indicates whether this row was affected by sampling. Sampled data is not 100% accurate. You can read more about sampling here: https://support.google.com/analytics/answer/2637192?hl=en#zippy=%2Ctematy-w-tym-artykule.


* **segment_id** <br>
Id of segment. Should be joined to `google_analytics.segment.segment_id`.


* **date** <br>
Date of the measurement.


* **landingpagepath** <br>
Path of the landing page (first page visited during session)


* **landingcontentgroup1** <br>
Landing group of the session Indicates type of page - e.g. `Homepage` or `Search Results with Calendars` .


* **devicecategory**<br>
User's device category. Possible values: `mobile`, `desktop` or `tablet`.


* **sessions**<br>
Unique sessions for this record. One users can have multiple sessions in one day.


* **transactions**<br>
Bookings made within the session.

* **productlistviews**<br>
Total number of search results displayed

* **productlistclicks**<br>
Number of clicks in the search results

* **productcheckouts**<br>
Number of booking flow entries as a result of click on search (directly from search or via doctor profile)







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
