---
layout: default
title: Search Saturation
parent: Google Analytics
nav_order: 8
---

# Search Saturation

---
### Short description

This table collects data about the saturation (number of doctors/facilities) on our search pages.

It shows how many people landed directly on our search and and how many facilities/doctors were displayed.

---
Data imported from Google Analytics v3 account (Main marketplace account).

---
### Columns

* **search_saturation_id**<br>
Table row unique id.


* **view_id**<br>
Id of Google Analytics view data was taken from, used to join a country to `google_analytics` data. = `google_analytics.view.view_id`.


* **is_sampled**<br>
Boolean. Indicates whether this row was affected by sampling. Sampled data is not 100% accurate. You can read more about sampling here: https://support.google.com/analytics/answer/2637192?hl=en#zippy=%2Ctematy-w-tym-artykule.


* **date**<br>
Date of the session.

* **landingpagepath**<br>
Url of the page user landed on.

* **dimension13**<br>
Number of doctor profiles displayed.

* **dimension14**<br>
Number of facility profiles displayed.

* **dimension15**<br>
Number of doctor **calendar** profiles displayed.

* **sessions**<br>
Number of sessions.

* **is_deleted**<br>


* **dw_md5**<br>
Technical, internal for Data Warehouse column


* **dw_created_at**<br>
Technical, internal for Data Warehouse column.
Indicates at what datetime the record was added to the table.


* **dw_updated_at**<br>
Technical, internal for Data Warehouse column.
Indicates at what datetime the record was changed.
If record was not change since added, *dw_updated_at* is equal to *dw_created_at*.

---
### Additional notes

For regular search pages, we display up to 20 doctor/facility profiles
For teleconsultation pages, up to 30.

As we limit number of results by addresses, but display them grouped to doctors/facilities, total number of profiles may be lower than max value, even if search is well saturated.
Best approach to determine saturation is number of calendar doctors (dimension15) divided by number of all doctors(dimension13)

---
### Related tables

`google_analytics.view` is necessary proxy to join data from `google_analytics` schema tables with proper country.

---
### Owner/contact person
@mikolaj.buzala@docplanner.com
