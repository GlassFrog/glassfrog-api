Roles
========


Get Person's Roles
----------

* `GET /person/[:id]/roles.xml` returns a list of roles and accountabilities for a particular person.

Returns 200 OK with a response body in the following format when successful:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<person>
  <id type="integer">516784585</id>
  <name>Joyce Bilbrey</name>
  <role>
    <circle-id type="integer">856843816</circle-id>
    <name>Principal Developer</name>
    <accountabilities>
      <accountability>
        <description>Voicing constraints to maintaining technical integrity so that business decisions which affect technical integrity can be made with full consciousness of the impact</description>
        <id type="integer">221350223</id>
      </accountability>
      <accountability>
        <description>Training others working within the codebase such that they could eventually fill the Principal Developer role if needed.</description>
        <id type="integer">324345070</id>
      </accountability>
      <accountability>
        <description>Defining and evolving an overall technical architecture, software design, and coding practices and processes for the product appropriate to the context and business needs</description>
        <id type="integer">591390822</id>
      </accountability>
      <accountability>
        <description>Maintaining the overall integrity of the product codebase to the extent practical given business constraints</description>
        <id type="integer">976665050</id>
      </accountability>
    </accountabilities>
  </role>
  [...]
</person>
```