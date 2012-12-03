Circles
========


Getting circles
----------

* `GET /circle.xml` will return all circles in the organization.

Returns 200 OK with a response body in the following format when successful:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<circles type="array">
  <circle>
    <id type="integer">856843816</id>
    <short-name>DDC</short-name>
  </circle>
  <circle>
    <id type="integer">708861762</id>
    <short-name>Sales</short-name>
  </circle>
  <circle>
    <id type="integer">582240928</id>
    <short-name>Ops</short-name>
  </circle>
  <circle>
    <id type="integer">1041583805</id>
    <short-name>GCC</short-name>
  </circle>
  <circle>
    <id type="integer">429327429</id>
    <short-name>Board</short-name>
  </circle>
</circles>
```

Getting circle roles
----------

* `GET /circle/[:id]/roles.xml` will return all custom roles in the circle specified by [:id].

It can be used to map the structure of the whole organization by first finding the circle ID of the Board circle from the method above, using this method to list the roles in the Board circle, and recursively traversing the circle structure using the supporting circle ID fields in the resulting role list.

Returns 200 OK with a response body in the following format when successful:


```xml
<?xml version="1.0" encoding="UTF-8"?>
<circle>
  <id type="integer">1041583805</id>
  <name>GCC</name>
  <role>
    <name>Development</name>
    <supporting-circle-id type="integer">856843816</supporting-circle-id>
    <purpose>Blow the client away with effortless software delivery.</purpose>
    <scopes>
      <scope>
        <description>Software business model</description>
        <id type="integer">775947396</id>
      </scope>
    </scopes>
    <accountabilities>
      <accountability>
        <description>Providing software solution implementation services.</description>
        <id type="integer">412385958</id>
      </accountability>
    </accountabilities>
  </role>
  <role>
    <name>Sales</name>
    <accountabilities>
      <accountability>
        <description>Selling software services.</description>
        <id type="integer">830864011</id>
      </accountability>
    </accountabilities>
  </role>
</circle>
```