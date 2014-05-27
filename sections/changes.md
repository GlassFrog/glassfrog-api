Release Notes
===============


May 28, 2014 - Initial API v3
------------------------

* format in json not xml
* API paths start with /API/v3/
* Mailing Lists now live on the /people endpoint, with a parameter of core role
* API keys are now associated with individual accounts (rather than the whole organization)
* Roles endpoints include core roles (Lead Link, Rep Link, Secretary, Facilitator)
* Added project, metrics, checklist_items

* This functionality replaces the mailing_list endpoint from v2. All Person resources now contain the email attribute.