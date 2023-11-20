---
layout: default
title: Booking Flow Pages
parent: Google Analytics
nav_order: 2
---

# Table name

---
### Short description

This table stores all basic information about unique pageviews on specific pages of the Booking Flow collected in Google Analytics.
Data imported from Google Analytics v3 account (Main marketplace account).
One row represents aggregated data of one page of the Booking Flow (which can be directly connected with a calendar, doctor and slot) in one day.

In this moment (14.01.2022) Booking Flow contains maximum 5 steps which will be explained in a **columns** section.


---
### Columns

* **booking_flow_pages_id**
Table row unique id.


* **view_id**
Id of Google Analytics view data was taken from, used to join a country to `google_analytics` data. = `google_analytics.view.view_id`.


* **is_sampled**
Boolean. Indicates whether this row was affected by sampling. Sampled data is not 100% accurate. You can read more about sampling here: https://support.google.com/analytics/answer/2637192?hl=en#zippy=%2Ctematy-w-tym-artykule.


* **date**
Date of the measurement.


* **devicecategory**
User's device category. Possible values: `mobile`, `desktop` or `tablet`.


* **contentgroup1**
Content group of page that event happened on. Indicates type of page - e.g. `Homepage` or `Search Results with Calendars`


* **pagepath**
Page path. Consctruction of the page path on the Booking Flow is:
/[constant_for_country_and_booking_flow_step]/[marketplace_doctor_id]/[marketplace_address_id]/[slot_timestamp]/[slot_id] .


* **browser**
User's browser.


* **campaign**
Sessions campaign. You can read more about campaigns here: https://support.google.com/analytics/answer/6205762?hl=en#zippy=%2Cin-this-article .


* **sourcemedium**
Session source and medium. You can read more about source and medium here: https://support.google.com/analytics/answer/6099206?hl=en .


* **uniquepageviews**
Unique pageviews of the page path.


* **is_deleted**


* **dw_md5**
Technical, internal for Data Warehouse column


* **dw_created_at**
Technical, internal for Data Warehouse column.
Indicates at what datetime the record was added to the table.


* **dw_updated_at**
Technical, internal for Data Warehouse column.
Indicates at what datetime the record was changed.
If record was not change since added, *dw_updated_at* is equal to *dw_created_at*.

---
### Additional notes

17.03.2021 new Booking Flow was introduced, format before that date is a legacy.

---
### Related tables

`google_analytics.view` is necessary proxy to join data from `google_analytics` schema tables with proper country.

From **pagepath** [marketplace_doctor_id] can be connected to stage_marketplace.doctor.id, [marketplace_address_id] to stage_marketplace.address.id .

---
### Owner/contact person
anna.oppenheim@docplanner.com / @mikolaj.buzala@docplanner.com
