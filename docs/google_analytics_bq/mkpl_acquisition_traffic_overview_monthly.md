---
layout: default
title: MKPL Acquisition traffic overview monthly
parent: Google Analytics BQ
---

# *mkpl_acquisition_traffic_overview_monthly*

## INTRODUCING NOTE

This table stores GA3 and GA4 WEB Marketplace data about acquisition traffic sources.

### TABLE LOGIC

The table is monthly aggregation of raw `spectrum.mkpl_acquisition_traffic_overview`.


### SOURCE TABLES

`spectrum.mkpl_acquisition_traffic_overview`

### CONTACT PERSON

If you have any questions, please contact *Miroslav Tkachenko* or other Analytics Engineers (Slack: *@Miroslav Tkachenko *, *@analytics-engineering-team*)

## COLUMNS DESCRIPTION
* **tool_data_source**

- indicates GA tool 'GA3' or 'GA4'

* **country**

- country code

* **month**

- event date aggregated to month


* **landing_page**

- landing page content group

* **device**

* **source**

- GA's source

* **medium**

- GA's medium

* **campaign**

- GA's campaign

* **previous_content_step**

- contains preceding ContentGroup1 value before checkout first entrance during the session. Value contains "missing data" if user entered checkout during session but there wasn't previous page available in the session. Please note that GA3 data for this column is more accurate than from GA4.

* **sessions**

- sum of sessions

* **transactions**

- sum of bookings

* **pageviews**

- sum of pageviews
