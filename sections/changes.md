Release Notes
===============

August 8, 2014 - v3.1 (operational systems sync)
------------------------------------------------
* Projects now include link, value, effort, and roi fields
* New actions: project create, update, archive, and delete endpoints
* Added Action and Trigger listing
* dates are output in utc

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

