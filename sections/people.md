People
===========

Retrieving People (GET)
----------------------

### Get all People in the Organization

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/people`

### Get a Specific Person

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/people/$PERSON_ID`


### Filtering by Circle (circle_id=)

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/people?circle_id=$CIRCLE_ID`

OR

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles/$CIRCLE_ID/people`


### Filtering by Role (role=)

The API supports retrieving all role-fillers of core roles in the organization.

##### Secretary

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/people?role=secretary`

##### Rep Link

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/people?role=replink`

##### Lead Link

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/people?role=leadlink`

##### Facilitator

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/people?role=facilitator`


#### Response Format

```json
{
    "people": [{
        "id": 911230097,
        "name": "Monica Wolfson",
        "email": "monica@example.com",
        "externalId": null
    }, {
        "id": 516784585,
        "name": "Joyce Bilbrey",
        "email": "joyce@example.com",
        "externalId": null
    }
}
```

#### Attribute Notes

* **external_id** (optional): for client use for storing ids from systems outside of GlassFrog


Adding People (POST)
----------------------

### Create a New Member of the Organization

`curl -H "X-Auth-Token: $API_KEY" -X POST -d '{"people":[{ "name":"Sally Benally", "email":"sally@example.com" }]}' https://glassfrog.holacracy.org/api/v3/people`

A successful POST returns status 200 with the newly created resource in the body:

```
{
    "people": [{
        "id": 657190835,
        "name": "Lawrence Copper",
        "email": "lawrence@example.com",
        "externalId": null
    }]
}
```

#### Emails Sent

Creating a Person through the API will email the new user with a welcome email and instructions for setting their password.

#### Permissions Notes

Only API_keys associated with accounts with admin permissions can add people to an organization.

#### Attributes
* __name__ _(required)_: full name of the person
* __email__ _(required)_: email of the person
* __external_id__ _(optional)_: id of the person from any external system



Updating People (PATCH/PUT)
---------------------------------

### Updating Name

`curl -H "X-Auth-Token: $API_KEY" -X PATCH -d '[{ "op":"replace","path":"/people/0/name", "value":"Sally Martinez"}]' https://glassfrog.holacracy.org/api/v3/people/$PERSON_ID`

### Updating Multiple Attributes

`curl -H "X-Auth-Token: $API_KEY" -X PATCH -d '[{ "op":"replace","path":"/people/0/name", "value":"Sally Martinez"},{"op":"replace","path":"/people/0/email", "value":"sally.martinez@example.com"}]' https://glassfrog.holacracy.org/api/v3/people/$PERSON_ID`

Returns 204 No Content on success.


Removing People (DELETE)
----------------------

### Remove a Person

`curl -H "X-Auth-Token: $API_KEY" -X DELETE https://glassfrog.holacracy.org/api/v3/people/$PERSON_ID`

returns 204 No Content on success.