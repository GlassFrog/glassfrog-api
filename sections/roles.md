Roles
========


Get Person's Roles
----------

* `GET /person/[:id]/roles.xml` returns a list of roles and accountabilities for a particular person.

Returns 200 OK with a response body in the following format when successful:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<person>
  <id type="integer">905931655</id>
  <name>Alan Logue</name>
  <role>
    <id type="integer">65842341</id>
    <circle-id type="integer">856843816</circle-id>
    <name>Circle Member</name>
  </role>
  <role>
    <id type="integer">436324341</id>
    <circle-id type="integer">856843816</circle-id>
    <name>Secretary</name>
    <election>2012-01-01</election>
    <purpose>Stabilize the Circle&#8217;s governance over time as a steward of the Circle&#8217;s formal records and record-keeping process.</purpose>
    <scopes>
      <scope>
        <description>All records required of a Circle under the Constitution, and any record-keeping processes and systems required to create and maintain such records for the Circle.</description>
        <id type="integer">1024896948</id>
      </scope>
    </scopes>
    <accountabilities>
      <accountability>
        <description>Maintaining all records of a Circle required by the Constitution, including capturing the outputs of the Circle&#8217;s Governance Process and Tactical Meetings, maintaining a compiled view of all governance currently in effect for the Circle, and maintaining a list of all operational elements currently being monitored in Tactical Meetings</description>
        <id type="integer">976665104</id>
      </accountability>
      <accountability>
        <description>Scheduling all regular and special meetings of the Circle which are explicitly required by the Constitution or by a Policy established by the Circle, in alignment with the terms of the Constitution and any relevant Policies of the Circle, and notifying all Circle Members of times and locations for meetings so scheduled</description>
        <id type="integer">976665105</id>
      </accountability>
      <accountability>
        <description>Interpreting the acting governance of the Circle upon request of a Circle Member as provided for in the Constitution, including ruling on matters of due process, procedure, and authority related to or granted under such governance or the Constitution itself</description>
        <id type="integer">976665106</id>
      </accountability>
    </accountabilities>
  </role>
</person>
```
