Release Notes
===============

August 25, 2015
---------------
* Files (empty for now) added for missing paths:
  * governance_meetings.md
  * organizations.md
  * policies.md
  * proposals.md
  * tactical_meetings.md
  * tensions.md

September 9, 2014 - (global checklist_items & metrics)
------------------------------------------------------
* Checklist Item and Metric endpoints now support create, update, and delete
* Can now create "global" Checklist Items and Metrics that show up on each circle in the organization

August 11, 2014 - v3.1 (personal systems sync)
------------------------------------------------
* You can now create, update, archive, and delete projects via the api.
* You can now list Actions and Triggers via the api, and filter them by created date
* Projects now include link, value, effort, and roi fields
* Default timezone for dates is now set to UTC instead of Eastern time.

May 28, 2014 - v3.0 (initial beta release)
------------------------------------------
* Implements all v2 functionality
* Format of GET responses and POST and PATCH bodies is json (not xml)
* API paths start with /api/v3
* Mailing Lists now live on the [people](people.md) endpoint, with a parameter of core role; all Person resources now contain the email attribute
* API keys are now associated with individual accounts (rather than the whole organization)
* [Roles](roles.md) endpoints include core roles (Lead Link, Rep Link, Secretary, Facilitator)
* Added readonly endpoints for [projects](projects.md), [metrics](metrics.md), and [checklist_items](checklist_items.md)
* Added ability to assign roles



