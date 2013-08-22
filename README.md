The Glassfrog API
====================


Requesting an API key
----------------

An organizational API key may be requested by emailing glassfrogsupport@holacracyone.com 


Making a request
----------------

All URLs start with `https://glassfrog.holacracy.org/api`. **SSL only**.  The full request path is formed by appending the method path to this address.

An organizational API key is required for all requests.  To include an API key in a request, append it to the URL as a parameter.

```
https://glassfrog.holacracy.org/api/v2/person.xml?api_key=123456789
```

Changes In Version 2
-----------------
* API paths start with /api/v2/
* Role information now includes:
	* Term expiration dates for elected roles
	* Role purposes
	* Scopes
	* Accountability IDs for structural roles (e.g. Lead Link)
* Person information no longer includes login (now obsolete)
* Can now return all roles in a circle, including supporting sub-circle IDs


API Methods
-----------------

* [Users](https://github.com/holacracybrian/glassfrog-api/blob/API_v2/sections/users.md)
* [Roles](https://github.com/holacracybrian/glassfrog-api/blob/API_v2/sections/roles.md)
* [Circles](https://github.com/holacracybrian/glassfrog-api/blob/API_v2/sections/circles.md)
* [Mailing Lists](https://github.com/holacracybrian/glassfrog-api/blob/API_v2/sections/mailing_lists.md)


Help us make it better
----------------------

Please tell us how we can make the API better.  If you have a specific feature request or if you found a bug, please email glassfrogsupport@holacracyone.com  
