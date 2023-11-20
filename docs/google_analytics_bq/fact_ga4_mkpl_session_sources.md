---
layout: default
title: GA4 MKPL Session Sources
parent: Google Analytics BQ
---

# spectrum.fact_ga4_mkpl_session_sources

---

### Short description

This table transforms raw event-level data from Google Analytics 4 (GA4) to a session-level overview. It combines multiple fields and extracts key traffic parameters, such as "source", "medium", "campaign", "content", and "keyword" to facilitate detailed analysis of marketing efforts.

The table includes timezone adjustments to ensure that timestamps accurately reflect local user activity. Each row uniquely represents a single event, identified by the `unified_session_id`, and contains information about the user and the specifics of the marketing interaction.

Please note that due to the extraction and transformation of data, certain considerations must be kept in mind when aggregating or further processing the data.

### TABLE LOGIC

The data is derived from GA4's raw event data. Event parameters ("source", "medium", "campaign", "content", "keyword") are isolated and brought to session-level granularity. Timestamps are translated into the relevant local timezone, determined by the country code linked to the session.

### SOURCE TABLES

- `ga-web-us.ga4_mkpl_web.events_raw`
- `ga-web-us.config.timezone`

### CONTACT PERSON

For any inquiries or clarifications, please reach out to *Miroslav Tkachenko* or the Analytics Engineering team (Slack: *@Miroslav Tkachenko*, *@analytics engineering*)

## COLUMNS DESCRIPTION

* **date** - The date when the session occurred. Extracted from the event timestamp.

* **timestamp** - Precise time when the session started, translated into the local timezone of the user, as indicated by the associated country code.

* **country_code** - The country code for the user's location during the session.

* **unified_session_id** - An amalgamated unique identifier for each session, formulated by combining the country code, user pseudo id, and session id.

* **mkpl_user_id** - The unique identifier for the user who initiated the session.

* **source** - The origin of the traffic that led the user to the session, such as a search engine or a specific online advertisement.

* **medium** - The general category of the source that led the user to the session, like "organic" for search engine traffic, or "email" for click-throughs from email marketing campaigns.

* **campaign** - Name of the specific marketing campaign associated with the session, helpful in tracking the performance of targeted marketing efforts.

* **content** - Identifies the specific content or variant of an advertisement that directed the user to the session, useful for A/B testing and similar analyses.

* **keyword** - The search term or keyword associated with the session, typically used in paid search engine marketing to understand which keywords are most effective in leading users to the website.
