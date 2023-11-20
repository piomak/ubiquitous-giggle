# *GOOGLE_ANALYTICS_BQ.PROFILE VIEWS*

## INTRODUCING NOTE

This table combines GA data on supply side users logins (doctors, clinic managers, secretaries). Data is taken from 3 environments - `mkpl`, `web saas` and `doctor app`

### TABLE LOGIC

Table aggregates logins daily logins data of given entity - doctor, clinic or secretary.

Table uses [GA session definition](https://support.google.com/analytics/answer/12798876?hl=en) and calculates `login_time` as time difference between first and last event attributed to logged in user during session (in minutes).

#### Important Info

- Multiscreen usage is not covered, so if user spent `2` minutes in `saas_app` while using `saas_web` in the very same time, `total_login_time` equal `4`
- MKPL side data is currently available only for doctors and clinics.
- For MKPL doctors that are `clinic` owners at the same time, all time spent in marketplace is attributed to both `clinic` and `doctor` user_type rows.
- Data for MKPL available from 06-2022, data for SaaS from 11-2022

### SOURCE TABLES

`spectrum.ga4_sessions_users`
`spectrum.ga4saas_sessions_users`
`spectrum.ga4doctorapp_sessions_users`

`saas.users`
`stage_marketplace.user_doctor_worker`

`dw.doctor`

`dw.facility`

### CONTACT PERSON

If you have any questions, please contact *Mikołaj Buzała* or other Analytics Engineers (Slack: *@meek*, *@analytics engineering*)

## COLUMNS DESCRIPTION

* **date**

* **country_code**

* **user_type**

- Type of the user
  - `doctor`, `clinic`, `secretary` or `clinic secretary`

* **dwh_doctor_id**

- `dw.doctor.doctor_id`, not null for `user_type = 'doctor'`

* **dwh_clinic_id**

- `dw.facility.facility_id` , not null for `user_type = 'clinic'`

* **saas_secretary_id**

- `saas.users.id` , not null for `user_type in ('secretary','clinic secretary')`

### AGGREGATES

* **total_login_time**

- Total time (in minutes) spent logged in. Sum of specific `*_login_time` columns.

* **mkpl_login_time**

- Time (in minutes) spent logged in to marketplace. Not calculated for `user_type in ('secretary','clinic secretary')`

* **saas_web_login_time**

- Time (in minutes) spent logged in to saas web.

* **saas_app_login_time**

- Time (in minutes) spent logged in to doctor app.

* **mkpl_logins**

- Number of separate sessions (page entrances separated by at least 30 minute break) with login to marketplace. Not calculated for `user_type in ('secretary','clinic secretary')`

* **saas_web_logins**

- Number of separate sessions (page entrances separated by at least 30 minute break) with login to web saas.

* **saas_app_logins**

- Number of separate sessions (app entrances separated by at least 30 minute break) with login to doctor app.
