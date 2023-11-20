# *GOOGLE_ANALYTICS_BQ.BOOKING_CONTEXT*

## INTRODUCING NOTE

This table stores modelled data about user booking context, such as booked entity, search activity before the booking and traffic source details. Data is available for `web` user bookings (patient app bookings are not included).

### TABLE LOGIC

The table enhances `spectrum.ga4_bookings` data with `spectrum.ga4_sessions` information and matches data with `dw.booking`. If there is no GA data available for given booking, it is not included in this table.


### SOURCE TABLES

`spectrum.ga4_bookings`

`spectrum.ga4_sessions`

`dw.booking`

### CONTACT PERSON

If you have any questions, please contact *Mikołaj Buzała* or other Analytics Engineers (Slack: *@meek*, *@analytics engineering*)

## COLUMNS DESCRIPTION
* **booking_date**


* **country_code**


* **dwh_booking_id**

  - `dw.booking.booking_id`


* **unified_session_id**

  - Google Analytics session ID of the booking


* **search_usage_status**

- Status of user's interaction with search in the session before the booking
  - `0` - no interaction with search
  - `1` - user visited search, but didn't click on any search result. (!!! Not available yet, currently marked as `0`)
  - `2` - user visited search and clicked at least one search result.
  - `3` - user entered booked entity's profile from search.
  - `4` - user entered booked entity's profile directly before the booking (last search click before the booking).

* **device_category**

- User's device category = `mobile` / `desktop` / `tablet`

* **profile_context**

- Type of the profile used to book a visit (or type of search result for bookings made directly from the SERP)
  - `doctor` or `facility`


* **traffic_campaign**

- Traffic source data. Value of the `utm_campaign` link parameter at session's start.


* **traffic_medium**

- Traffic source data. Value of the `utm_medium` link parameter at session's start.


* **traffic_source**

- Traffic source data. Value of the `utm_source` link parameter at session's start.


* **traffic_content**

- Traffic source data. Value of the `utm_content` link parameter at session's start.


* **landing_page**

- URL of the session's landing page

* **landing_page_content_group**

- Content group of the session's landing page

* **landing_page_doctor_id**

- If landing page of the session was doctor profile = `stage_marketplace.doctor.id`

* **landing_page_clinic_id**

- If landing page of the session was clinic profile = `stage_marketplace.clinic.id`
