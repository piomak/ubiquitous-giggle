# Google Analytics Bookings Tables

---
### Short description

This set of tables store all transactions recorded in Google Analytics and attributed to specific traffic group.
<br><br>Attribution is based on the traffic source and medium (UTM parameters) in following tables:
- `bookings_gmb` - google my business cards
- `bookings_sm_link_v1` and `_v2` - Social media links from Doctor 360. We do use 2 tables, as there are 2 separate link tagging mechanisms.
- `bookings_widget_js` - JavaScript widgets on doctor pages
- `bookings_widget_link` - plain links on doctor pages

Attribution is based on user behavior in following tables:
- `bookings_search` - user clicked on at least one doctor on search during the session.

Precise criteria for each table are defined in related `google_analytics.segment` entry.

---
Data imported from Google Analytics v3 account (Main marketplace account).

Results from this tables can be left joined to `dw.booking.source_mkpl_id` or `stage_marketplace.visit_booking_id` to flag bookings coming from particular source.

---
### Columns

* **booking_search_id**<br>
Table row unique id.


* **view_id**<br>
Id of Google Analytics view data was taken from, used to join a country to `google_analytics` data. = `google_analytics.view.view_id`.


* **is_sampled**<br>
Boolean. Indicates whether this row was affected by sampling. Sampled data is not 100% accurate. You can read more about sampling here: https://support.google.com/analytics/answer/2637192?hl=en#zippy=%2Ctematy-w-tym-artykule.


* **segment_id**<br>
`google_analytics.segment.id` used to filter the data.

* **transactionid**<br>
Id of transaction (booking) = `stage_marketplace.visit_booking.id`

* **transactions**<br>
Number of transactions. **Should not be used** as it's recorded only due to technical limitations. Always use just `count distinct (transactionid)` to get number of transactions.

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
`google_analytics.segment` defines the segment used in this table
`stage_marketplace.visit_booking` / `dw.booking.` are the main tables data from `bookings_` is joined to.
---
### Owner/contact person
anna.oppenheim@docplanner.com / @mikolaj.buzala@docplanner.com
