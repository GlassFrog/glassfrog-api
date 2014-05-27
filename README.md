Glassfrog API v3 beta
=====================

Overview
--------

### Status

The v3 API is in beta.  The current stable version is [v2](../../tree/API_v2).

With v3, we've upgraded the API to use and return json.  When v3 is finalized, v2 will be deprecated and new features will be added only to v3.
If you are currently using v2, you can try out v3 at the same time without affecting your current integrations.
Please note that since v3 is in beta, the API endpoints are subject to change.
While we will make reasonable attempts to keep them stable, we may still be changing any endpoint as we get feedback on usage.

### Recent Changes

For details on the latest changes see [Release Notes](sections/changes.md).

### Authentication

Authentication for the API is provided by API keys which can be found in GlassFrog in the profile/account dropdown under your name in the top right of the application.
API keys provide full access to your GlassFrog account with the same permissions that you have.
Keep them safe like you would your password! Generating and revoking keys is easy, create one for each application you need to integrate with, and it will be easier to replace later if a specific key is compromised.


### Design

* API v3 is designed to follow the emerging [json-API](http://jsonAPI.org/format/) standard

Using the API
----------------

### Making a request

All URLs start with `https://glassfrog.holacracy.org/API/v3/`. **SSL only**.
The full request path is formed by appending the method path to this address.

An API key is required for all requests.  To include an API key in a request, append it to the URL as a parameter:

```
curl "https://glassfrog.holacracy.org/api/v3/people?api_key=$API_KEY"
```

Or pass it as the value of the `X-Auth-Token` header:

```
curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/people
```

### PATCH requests

GlassFrog API uses PATCH for updating resource documents, however, PUT may be used in place of PATCH

PATCH / PUT requests follow the jsonapi formatting standards. See "Updating a Document" and "Relationships" sections of the standards
for more details: [http://jsonapi.org/format](http://jsonapi.org/format).

**Transactional updates:** If one operation in a multi-operation requests fails then the whole request will fail and none of the operations will be processed.


### Responses

#### JSON Data
API v3 is designed to follow the emerging [json-API](http://jsonAPI.org/format/) standard
Relationships between objects are represented in the 'links' attribute, and contain ids that reference other objects.
Referenced objects can be found in under the 'linked' top level key.

```json
{
  "linked": {
    "people": [
      {
        "id": 811765527,
        "name": "Carlos Aldrich",
        "email": "carlos@example.com",
        "external_id": null
      },
    ]
  },
  "circles": [
    {
      "id": 582240928,
      "name": "Operations",
      "links": {
        "people": [
          811765527
        ]
      }
    }
  ]
}
```

GlassFrog API uses standard HTTP response codes to indicate various states:

#### Success
* 200 - Success:  Response body contains requested or updated data.
* 204 - No Content: Update or Delete was performed as requested.

#### Errors
* 401 - Unauthenticated: No API key or invalid API key provided
* 403 - Unauthorized:  Your API key is good but your user account doesn't have permission to perform the specified action.
* 404 - Not Found: Couldn't find a resource you requested, or invalid URL
* 422 - Unprocessable Entity: There was a problem with the data you provided, either we couldn't parse it or it specified an invalid state.
* 500 - Server Error: Unhandled exception


### API Endpoint details

* [People](sections/people.md)
* [Roles](sections/roles.md)
* [Circles](sections/circles.md)
* [Projects](sections/projects.md)
* [Checklist Items](sections/checklist_items.md)
* [Metrics](sections/metrics.md)


Help us make it better
-----------------------

Please tell us how we can make the API better.  If you have a specific feature request or if you found a bug, please email glassfrog-api@holacracyone.com
