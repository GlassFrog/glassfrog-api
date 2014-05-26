Users
========


Getting members of the organization
------------------------------------

* `GET /person.xml` returns a list of people who are members of the organization.

Returns 200 OK with a response body in the following format when successful:

```json
{
    "people": [{
        "id": 911230097,
        "name": "Monica Wolfson",
        "email": "monica@fictional.com",
        "externalId": null
    }, {
        "id": 380424410,
        "name": "Louis Hoppe",
        "email": "louis@fictional.com",
        "externalId": null
    }, {
        "id": 811765527,
        "name": "Carlos Aldrich",
        "email": "carlos@fictional.com",
        "externalId": null
    }, {
        "id": 657190835,
        "name": "Lawrence Copper",
        "email": "lawrence@fictional.com",
        "externalId": null
    }, {
        "id": 516784585,
        "name": "Joyce Bilbrey",
        "email": "joyce@fictional.com",
        "externalId": null
    }
}
```

Filtering by role
-------------------

* this functionality replaces the mailing_list endpoint from v2.  it allows filtering of people by core role name (facilitator, replink, leadlink, secretary)

* `GET /people?role=secretary` returns list of all secretaries in the organization

```json
{
    "people": [{
        "id": 657190835,
        "name": "Lawrence Copper",
        "email": "lawrence@fictional.com",
        "externalId": null
    }, {
        "id": 905931655,
        "name": "Alan Logue",
        "email": "alan@fictional.com",
        "externalId": "34"
    }, {
        "id": 943584124,
        "name": "Maureen Linton",
        "email": "maureen@fictional.com",
        "externalId": null
    }]
}
```



Creating a user
----------------

* `POST /person.xml` creates a new member of the organization. The external_user_id fields is optional

```
/person.xml?api_key=123456789&person[email]=test%40test.com&person[name]=Test&person[password]=test&person[password_confirmation]=test&person[external_user_id]=123
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
----------

* `GET /person/[:id].xml?api_key=123456789` returns information about the person specified by [:id].

Returns 200 OK with a response body in the following format when successful:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<person>
  <email>monica@fictional.com</email>
  <id type="integer">911230097</id>
  <name>Monica Wolfson</name>
  <external-user-id>123</external-user-id>
</person>
```

Updating a user
----------

* `PUT /person/[:id].xml` updates the person specified by [:id].

```
/person/[:id].xml?api_key=123456789&person[email]=monica%40fictional.com&person[name]=Monica+Wolfson&person[external_user_id]=345
```

Returns 200 OK with a blank response body when successful.


Removing a user
----------

* `DELETE /person/[:id].xml` removes the person specified by [:id], and unassigns them from all roles.

```
/person/[:id].xml?api_key=123456789
```

Returns 200 OK with a blank response body when successful.
