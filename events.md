# Events

---
### Short description

This table stores all basic information about event collected in Google Analytics.

Data imported from Google Analytics v3 account (Main marketplace account).

One row represents aggregated data of one event, on one page type on one type of device in one day.


---
### Owner/contact person
mikolaj.buzala@docplanner.com / anna.oppenheim@docplanner.com

---
### Columns
- `events_id`<br>
Table row unique id
- `view_id`<br>
Id of Google Analytics view data was taken from, used to join a country to `google_analytics` data. = `google_analytics.view.view_id`
- `is_sampled`<br>
Boolean. Indicates whether this row was affected by sampling. Sampled data is not 100% accurate. You can read more about sampling here: https://support.google.com/analytics/answer/2637192?hl=en#zippy=%2Ctematy-w-tym-artykule
- `date`<br>
Date of the measurement
- `devicecategory`<br>
  User's device category. Possible values: `mobile`, `desktop` or `tablet`
- `eventcategory`<br>
  Category of the event.
- `eventaction`<br>
  Action of the event.
- `eventlabel`<br>
  Label of the event.
- `contentgroup1`<br>
  Content group of page that event happened on. Indicates type of page - e.g. `Homepage` or `Search Results with Calendars`
- `totalevents`<br>
  Total number of events.
- `uniqueevents`<br>
Unique number of events. Unique Events is a metric that counts the number of events with distinct Event attributes that occur within a single user session.
- `is_deleted`
Whether this event was deleted.
- `dw_md5`
Technical, internal for Data Warehouse column
-`dw_created_at`
Technical, internal for Data Warehouse column.
Indicates at what datetime the record was added to the table.
-`dw_updated_at`
Technical, internal for Data Warehouse column.
Indicates at what datetime the record was changed.
If record was not change since added, *dw_updated_at* is equal to *dw_created_at*.

---
### Additional notes

---
### Related tables

`google_analytics.view` is necessary proxy to join data from `google_analytics` schema tables with proper country
