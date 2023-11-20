---
layout: default
title: Search Query Type
parent: Google Analytics
nav_order: 7
---

# Search Query Type

---
### Short description

This table collects data about all search impressions (displaying single doctor/clinic on search) and it's performance (clicks,booking flow enters, bookings) split by search query type (listing type and all criteria used in search query).

---
Data imported from Google Analytics v3 account (Main marketplace account).

---
### Columns

* **search_query_type_id**<br>
Table row unique id.


* **view_id**<br>
Id of Google Analytics view data was taken from, used to join a country to `google_analytics` data. = `google_analytics.view.view_id`.


* **is_sampled**<br>
Boolean. Indicates whether this row was affected by sampling. Sampled data is not 100% accurate. You can read more about sampling here: https://support.google.com/analytics/answer/2637192?hl=en#zippy=%2Ctematy-w-tym-artykule.


* **date**<br>


* **productlistname**<br>
Name of Enhanced Ecommerce product list = search results list type.<br>
  <br>The name structure is as follows `[search results type]` `[search list calendar status]` `[search query criteria]`
  <br>They are as follows:
  - Search Results type = `Regular` for regular placements, `FC` for First class placements, `NewDoctor` for New doctor placements
  - Search Results calendar status = `Calendar` if there is at least one calendar doctor on displayed page or `Non-calendar`
  - Search Query Criteria = `+` separated list of all criteria used in the search query e.g. `specialization + location + services + languages`

* **productlistviews**<br>
Total number of results displayed

* **productlistclicks**<br>
Number of clicks in the results

* **productcheckouts**<br>
Number of booking flow entries as a result of click on search (directly from search or via doctor profile)

* **uniquepurchases**<br>
Number of bookings

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

---
### Related tables

`google_analytics.view` is necessary proxy to join data from `google_analytics` schema tables with proper country.

---
### Owner/contact person
@mikolaj.buzala@docplanner.com
