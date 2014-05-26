People
===========
* in organization
* in circle
* in role
* /roles
* /role=leadlink
* /role=replink
* /role=secretary
* /role=facilitator
* CREATE
* UPDATE
* DELETE
* note: externalId is an optional field for use when integrating with systems outside GlassFrog.

Getting members of the organization
-----------------------------------



* `GET /person` returns a list of people who are members of the organization.

Returns 200 OK with a response body in the following format when successful:

```json
{
    "people": [{
        "id": 911230097,
        "name": "Monica Wolfson",
        "email": "monica@example.com",
        "externalId": null
    }, {
        "id": 380424410,
        "name": "Louis Hoppe",
        "email": "louis@example.com",
        "externalId": null
    }, {
        "id": 811765527,
        "name": "Carlos Aldrich",
        "email": "carlos@example.com",
        "externalId": null
    }, {
        "id": 657190835,
        "name": "Lawrence Copper",
        "email": "lawrence@example.com",
        "externalId": null
    }, {
        "id": 516784585,
        "name": "Joyce Bilbrey",
        "email": "joyce@example.com",
        "externalId": null
    }
}
```

### Filtering by role


* this functionality replaces the mailing_list endpoint from v2.  it allows filtering of people by core role name (facilitator, replink, leadlink, secretary)

* `GET /people?role=secretary` returns list of all secretaries in the organization

```json
{
    "people": [{
        "id": 657190835,
        "name": "Lawrence Copper",
        "email": "lawrence@example.com",
        "externalId": null
    }, {
        "id": 905931655,
        "name": "Alan Logue",
        "email": "alan@example.com",
        "externalId": "34"
    }, {
        "id": 943584124,
        "name": "Maureen Linton",
        "email": "maureen@example.com",
        "externalId": null
    }]
}
```



Creating a person
----------------
#### Permissions
only API_keys associated with accounts with admin permissions can add people to an organization

* `POST /person` creates a new member of the organization. The POST body should contain the data for the person in the following format:

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

Returns 200 OK with a response body in the following format when successful:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<person>
  <email>test@test.com</email>
  <id type="integer">1067646470</id>
  <name>Test</name>
  <external-user-id>123</external-user-id>
</person>
```

Retrieving a user
-----------------

* `GET /person/[:id].xml?API_key=123456789` returns information about the person specified by [:id].

Returns 200 OK with a response body in the following format when successful:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<person>
  <email>monica@example.com</email>
  <id type="integer">911230097</id>
  <name>Monica Wolfson</name>
  <external-user-id>123</external-user-id>
</person>
```

Updating a user
----------

* `PUT /person/[:id].xml` updates the person specified by [:id].

```
/person/[:id].xml?API_key=123456789&person[email]=monica%40example.com&person[name]=Monica+Wolfson&person[external_user_id]=345
```

Returns 200 OK with a blank response body when successful.


Removing a user
----------

* `DELETE /person/[:id].xml` removes the person specified by [:id], and unassigns them from all roles.

```
/person/[:id].xml?API_key=123456789
```

Returns 200 OK with a blank response body when successful.
