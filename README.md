Glassfrog API v3 beta
=====================

Please note!  The v3 API is in a testing period and subject to breaking changes at any time.

API keys
--------

API keys for v3 are found in GlassFrog in the profile/account dropdown under your name in the top right of the application.


Making a request
----------------

All URLs start with `https://glassfrog.holacracy.org/api/v3/`. **SSL only**.  The full request path is formed by appending the method path to this address.
An API key is required for all requests.  To include an API key in a request, append it to the URL as a parameter,
or pass it as the value of the `X-Auth-Token` header.

```
https://glassfrog.holacracy.org/api/v3/people?api_key=123456789
```

Changes In Version 3
--------------------

* API v3 is a json api designed to follow the emerging [json-api](http://jsonapi.org/format/) standard
* API paths start with /api/v3/


API Endpoints
-------------

* [People](https://github.com/holacracybrian/glassfrog-api/blob/API_v3/sections/users.md)
* [Roles](https://github.com/holacracybrian/glassfrog-api/blob/API_v3/sections/roles.md)
* [Circles](https://github.com/holacracybrian/glassfrog-api/blob/API_v3/sections/circles.md)
* [Mailing Lists](https://github.com/holacracybrian/glassfrog-api/blob/API_v3/sections/mailing_lists.md)


Help us make it better
-----------------------

Please tell us how we can make the API better.  If you have a specific feature request or if you found a bug, please email glassfrog-api@holacracyone.com
