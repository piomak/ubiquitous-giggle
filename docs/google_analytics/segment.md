# Segment

---
### Short description

Dictionary table for data in `google_analytics` schema.

Stores information about GA segments used to pull filtered data.

Segment is a set of criteria, that original data need to meet to be extracted.

Segments are used to narrow the data from given view.
E.g. to pull the data just for sessions from given traffic source or starting from specific page type.

Read more about segments here: https://support.google.com/analytics/answer/3123951?hl=en#zippy=%2Cin-this-article



---
### Owner/contact person
mikolaj.buzala@docplanner.com / anna.oppenheim@docplanner.com

---
### Columns
- `segment_id`<br>
Id of segment. Used in `google_analytics` tables that pulls filtered data to identify the segment.


- `name`<br>
  Our intenal name of the segment, describes what kind of


- `definition`<br>
Google Analytics definition of the segment. Read more about it here: https://developers.google.com/analytics/devguides/reporting/core/v3/reference#segment


- `dw_created_at`
Technical, internal for Data Warehouse column.
Indicates at what datetime the record was added to the table.


- `dw_updated_at`
Technical, internal for Data Warehouse column.
Indicates at what datetime the record was changed.
If record was not change since added, *dw_updated_at* is equal to *dw_created_at*.

---
### Additional notes

Segments may be created in Google Analytics User Interface or just using the API reference.
