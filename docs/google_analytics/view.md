# View

---
### Short description

Main dictionary table for data in `google_analytics` schema. Contains information about Google Analytics accounts, properties and views used to pull Google Analytics data.



---
### Owner/contact person
mikolaj.buzala@docplanner.com / anna.oppenheim@docplanner.com

---
### Columns
- `view_id`<br>
Id of Google Analytics view. View is a single google analytics dataset.
- `country_id`<br>
Id of country that view is related to. Equals `dw.country.country_id`
- `ga_account`<br>
Name of Google Analytics account, that view is part of.Visible in GA User Interface. `v3` is our cur current main reporting account. `v2` is legacy one, not used anymore.
- `property_name`<br>
Name of Google Analytics property, that view is part of.Visible in GA User Interface.
- `view name`<br>
Name of the view. Visible in GA User Interface.
- `property_scope`<br>
Scope of the property. Describes general purpose of given property (e.g. marketplace or doctors)
- `view_scope`<br>
Scope of the view. Describes if view shows all the data for given property (`General`) or just some part of it.
- `property_id`<br>
Id of Google Analytics property.
- `created_at`
Technical, internal for Data Warehouse column.
Indicates at what datetime the record was added to the table.
- `updated_at`
Technical, internal for Data Warehouse column.
Indicates at what datetime the record was changed.
If record was not change since added, *updated_at* is equal to *created_at*.
- `country_code`<br>
2-letter ISO code of a country. Equals `dw.country.country_code`

---
### Additional notes
- one property collects all the views for one country in one scope.
---
### Related tables

All tables in `google_analytics` schema are related to `view_id` columns.
