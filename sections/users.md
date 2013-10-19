Users
========


Getting members of the organization
----------

* `GET /person.xml` returns a list of people who are members of the organization.

Returns 200 OK with a response body in the following format when successful:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<people type="array">
  <person>
    <email>joyce@fictional.com</email>
    <id type="integer">516784585</id>
    <name>Joyce Bilbrey</name>
  </person>
  <person>
    <email>robert@fictional.com</email>
    <id type="integer">957904360</id>
    <name>Robert Ryder</name>
    <external-user-id>853</external-user-id>
  </person>
  <person>
    <email>olivia@fictional.com</email>
    <id type="integer">209365805</id>
    <name>Olivia Battle</name>
  </person>
  <person>
    <email>marlene@fictional.com</email>
    <id type="integer">251465608</id>
    <name>Marlene Mclane</name>
  </person>
  [...]
</people>
```

Creating a user
----------

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
