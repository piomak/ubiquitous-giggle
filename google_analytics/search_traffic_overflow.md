# Search Traffic Overflow

---
### Short description

This table shows total number of sessions that used particular search page types.

---
Data imported from Google Analytics v3 account (Main marketplace account).

---
### Columns

* **search_traffic_overflow_id**<br>
Table row unique id.


* **view_id**<br>
Id of Google Analytics view data was taken from, used to join a country to `google_analytics` data. = `google_analytics.view.view_id`.


* **is_sampled**<br>
Boolean. Indicates whether this row was affected by sampling. Sampled data is not 100% accurate. You can read more about sampling here: https://support.google.com/analytics/answer/2637192?hl=en#zippy=%2Ctematy-w-tym-artykule.


* **date**<br>


* **browser**<br>
User browser name


* **contentgroup3**<br>
Search page type
  <br>The name structure is as follows `[search list calendar status]` `[search query criteria]` `[url type]` `[search page number]`
  <br>They are as follows:
  - Search Results calendar status = `calendar` if there is at least one calendar doctor on displayed page or `non-calendar`
  - Search Query Criteria = `+` separated list of all criteria used in the search query e.g. `specialization + location + services + languages`
  - Url type = `nice` for SEO-friendly urls like `/ginekolog/warszawa`, `raw` for search-engine raw URLs like `szukaj?q=ginekolog&loc=Warszawa&filters%5Bspecializations%5D%5B%5D=57` (both displays exactly same page)
  - Page number = number of search page

* **contentgroupuniqueviews3**<br>
Number of unique pageviews. You can read more about their definition here: https://sortable.com/blog/ad-ops/pageviews-vs-sessions-vs-unique-pageviews/


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
