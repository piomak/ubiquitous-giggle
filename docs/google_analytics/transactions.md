---
layout: default
title: Booking Flow Pages
parent: Transactions
nav_order: 17
---


# Transactions

---
### Short description

This table stores all basic information about transactions collected in Google Analytics.

Transaction is an equivalent of user booking.

Data imported from Google Analytics v3 account (Main marketplace account).

One row represents one tracked user booking with additional information about the booking source.


---
### Owner/contact person
mikolaj.buzala@docplanner.com / anna.oppenheim@docplanner.com

---
### Columns
- `transactions_id`<br>
Table row unique id
- `view_id`<br>
Id of Google Analytics view data was taken from, used to join a country to `google_analytics` data. = `google_analytics.view.view_id`
- `is_sampled`<br>
Boolean. Indicates whether this row was affected by sampling. Sampled data is not 100% accurate. You can read more about sampling here: https://support.google.com/analytics/answer/2637192?hl=en#zippy=%2Ctematy-w-tym-artykule
- `date`<br>
Date of the measurement
- `source`<br>
Source of the user session. Equal to `utm_source` url parameter if one exists.
- `medium`<br>
Medium of the user session. Equal to `utm_medium` url parameter if one exists.
- `campaign`<br>
Campaign of the user session. Equal to `utm_campaign` url parameter if one exists.
- `keyword`<br>
Keyword of the user session. Equal to `utm_term` url parameter if one exists.
- `transactionid`<br>
Id of transaction. Equal to `stage_marketplace.visit_booking.id`
- `transactions`<br>
Number of transactions. Useless data, pulled only due to GA API limitations. Do not use it.
- `is_deleted`

- `dw_md5`
Technical, internal for Data Warehouse column.
-`dw_created_at`
Technical, internal for Data Warehouse column.
Indicates at what datetime the record was added to the table.
- `dw_updated_at`
Technical, internal for Data Warehouse column.
Indicates at what datetime the record was changed.
If record was not change since added, *dw_updated_at* is equal to *dw_created_at*.

---
### Additional notes

This data may be different than data stored in booking sources as collection method differs.
If combined with `dw.booking` table it should be used as suplementary source and be left joined. Not other way around

---
### Related tables

`google_analytics.view` is necessary proxy to join data from `google_analytics` schema tables with proper country
