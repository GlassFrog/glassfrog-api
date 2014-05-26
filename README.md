Glassfrog API v3 beta
=====================

Status
--------
The v3 API is in beta.  The current stable version is [v2](/holacracyone/glassfrog-api/tree/API_v3)

With v3, we've upgraded the api to use and return json, and we are planning to only add new functionality to v3 in the future.
If you are currently using v2, you can also try out v3 at the same time without affecting your current integrations.
Please note that since v3 is in beta, the api endpoints are subject to change.
While we will make reasonable attempts to keep them stable, we may still be changing any endpoint as we get feedback on usage.


API v3 is a json api designed to follow the emerging [json-api](http://jsonapi.org/format/) standard

API keys
--------

API keys for v3 are found in GlassFrog in the profile/account dropdown under your name in the top right of the application.
API keys provide full access to your GlassFrog account with the same permissions that you have. Keep them safe like you would your password! Generating and revoking keys is easy, create one for each application you need to integrate with, and it will be easier to replace later if a specific key is compromised.

Making a request
----------------

All URLs start with `https://glassfrog.holacracy.org/api/v3/`. **SSL only**.  The full request path is formed by appending the method path to this address.
An API key is required for all requests.  To include an API key in a request, append it to the URL as a parameter,
or pass it as the value of the `X-Auth-Token` header.

```
https://glassfrog.holacracy.org/api/v3/people?api_key=123456789
```

Changes In Version 3  (from v2)
--------------------
* [Release Notes](sections/changes.md)

API Endpoints
-------------

* [People](sections/people.md)
* [Roles](sections/roles.md)
* [Circles](sections/circles.md)
* [Projects](sections/projects.md)
* [Checklist Items](sections/checklist_items.md)
* [Metrics](sections/metrics.md)


Help us make it better
-----------------------

Please tell us how we can make the API better.  If you have a specific feature request or if you found a bug, please email glassfrog-api@holacracyone.com
