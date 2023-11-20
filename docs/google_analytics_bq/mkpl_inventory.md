# *GOOGLE_ANALYTICS.MKPL_INVENTORY*

## INTRODUCING NOTE

This table is designed for inventory analysis. It contains data about number of sessions, users and bookings we had in each month per each `search_specialization` + `search_location` pair.

Please note that metrics such as users and sessions has been aggregated for each row separately, meaning that summing them up won't be accurate.


### TABLE LOGIC

This table data is based on GA's `view_item_list` events.

### SOURCE TABLES

- `spectrum.ga4_search_list_views`
- `spectrum.ga4_bookings`
- `spectrum.ga4_sessions`

### CONTACT PERSON

If you have any questions, you can contact *Ania Chabulada*, *Miroslav Tkachenko* or other Analytics Engineers (Slack: *@Ania Chabulada*, *@Miroslav Tkachenko*, *@analytics engineering*)

## COLUMNS DESCRIPTION

* **landing_content_group** – Session scoped landing page content group.


* **search_mkpl_specialization_id** = `stage_marketplace.specialization.id` – ID of specialization that was searched by user.


* **search_location** – location name.

Due to search mechanism, one physical location can get multiple different values ( e.g. for Barcelona it may equal `Barcelona`, `Barcelona, Barcelona` etc.)

* **identified_users** – count of logged-in users


* **users** – count of all users.


* **sessions** – count of sessions.


* **listing_searches** – count of performed searches.


* **clicks** – count of performed clicks on search listing pages.


* **transactions** – count of booking.
