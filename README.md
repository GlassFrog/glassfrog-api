The Glassfrog API
====================


Making a request
----------------

All URLs start with `https://glassfrog.holacracy.org/api`. **SSL only**.  The full request path is formed by appending the method path to this address.

An organizational API key is required for all requests.  To include an API key in a request, append it to the URL as a parameter.

```
https://glassfrog.holacracy.org/api/person.xml?api_key=123456789
```


No JSON, just XML
-----------------

We only support XML for serialization of data.  All API URLs end in .xml to indicate that they return XML.


API ready for use
-----------------

* [Users](https://github.com/karlhigley/Glassfrog-API-Documentation/blob/master/sections/users.md)
* [Roles](https://github.com/karlhigley/Glassfrog-API-Documentation/blob/master/sections/roles.md)
* [Circles](https://github.com/karlhigley/Glassfrog-API-Documentation/blob/master/sections/circles.md)
* [Mailing Lists](https://github.com/karlhigley/Glassfrog-API-Documentation/blob/master/sections/mailing_lists.md)


API still under development
---------------------------


Help us make it better
----------------------

Please tell us how we can make the API better.  If you have a specific feature request or if you found a bug, please use GitHub issues.  For improvements to the documentation, fork this repository and send a pull request with improvements.  