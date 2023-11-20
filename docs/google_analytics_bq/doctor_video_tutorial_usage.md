# *GOOGLE_ANALYTICS_BQ.DOCTOR_VIDEO_TUTORIAL_USAGE*

## INTRODUCING NOTE

This table stores modelled and aggregated data about the usage of doctor video tutorial saas feature.

### TABLE LOGIC

This table aggregates data from `spectrum.ga4saas_doctor_video_events` table.
Table aggregates interactions of one type/related to specific video content withing one day.

### SOURCE TABLES

`spectrum.ga4saas_doctor_video_events`


### CONTACT PERSON

Technical questions, please contact *Mikołaj Buzała* or other Analytics Engineers (Slack: *@meek*, *@analytics engineering*)
Feature's business context, contact *Alberto Castro*.

## COLUMNS DESCRIPTION

* **country_code**

* **date**
  - Date of the interaction.

## USER IDENTIFICATION

* **saas_user_id**

 - SaaS ID of the user who interacted with video-library.

* **dwh_doctor_id**

 - DWH Doctor ID of the user who interacted with video-library. `Null` if user is not a doctor.

* **mkpl_doctor_id**

 - MKPL Doctor ID of the user who interacted with video-library. `Null` if user is not a doctor.


### Event data

* **event_type**

- `visit-library` = user visited video tutorials library
- `open-video` = user opened specific video's page
- `watch-video` = user interacted with video player

* **video_category**

- Category of a video user interacted with. Not `null` for `open-video` and `watch-video` events.

* **video_key**

- ID of a video user interacted with. Not `null` for `open-video` and `watch-video` events.

* **interaction_start**

- Timestamp of the first interaction in a day.

* **watch_time**

- Not `null` for `watch-video` events. Maximum recorded video watch time. E.g. if doctor paused video after 30 seconds = `30`

* **watch_percent**

- Not `null` for `watch-video` events. Maximum recorded video watch time divided by the total length of the video. E.g. if doctor paused video of total length of 300 seconds after 30 seconds = `0.1`
