Circles
========


Getting circles
----------

* `GET /circle.xml` will return all circles in the organization.

Returns 200 OK with a response body in the following format when successful:

```
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

