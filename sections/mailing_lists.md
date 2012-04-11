Mailing lists
========


Mailing list methods return a list of users that fill certain kinds of roles in the organization: Lead Links, Rep Links, Facilitators, Secretaries, Circle Members (of a particular circle.)  Each method returns 200 OK and an array of people in the following format when successful:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<people type="array">
  <person>
    <name>Joyce Bilbrey</name>
    <id type="integer">516784585</id>
    <email>joyce@fictional.com</email>
  </person>
  <person>
    <name>Vivian Eagle</name>
    <id type="integer">656753429</id>
    <email>vivian@fictional.com</email>
  </person>
  <person>
    <name>Faye Falco</name>
    <id type="integer">892961214</id>
    <email>faye@fictional.com</email>
  </person>
  <person>
    <name>Alan Logue</name>
    <id type="integer">905931655</id>
    <email>alan@fictional.com</email>
  </person>
  <person>
    <name>Monica Wolfson</name>
    <id type="integer">911230097</id>
    <email>monica@fictional.com</email>
  </person>
</people>
```


Get Lead Links
----------

* `GET /lead_links.xml` will return the Lead Links of all circles in the organization


Get Rep Links
----------

* `GET /rep_links.xml` will return the Rep Links of all circles in the organization


Get Facilitators
----------

* `GET /facilitators.xml` will return the Facilitators of all circles in the organization


Get Secretaries
----------

* `GET /secretaries.xml` will return the Secretaries of all circles in the organization

Get Circle Members
----------

* `GET /circle/[:id]/mailing_list.xml` will return all members of the circle identified by [:id]
