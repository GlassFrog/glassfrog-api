Projects
==========

Retrieving Projects (GET)
--------------------------

### Getting all Projects on a Circle

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles/$CIRCLE_ID/projects`

OR

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/projects?circle_id=$CIRCLE_ID`


#### Response Format

```json
"linked": {
    "circles": [
        {
            "id": 856843816,
            "links": {},
            "name": "Development",
            "short_name": "DDC",
            "strategy": "Emphasize \"Working Software\", even over \"Comprehensive Documentation\""
        }
    ],
    "people": [
        {
            "email": "monica@example.com",
            "external_id": null,
            "id": 911230097,
            "name": "Monica Wolfson"
        }
    ],
    "roles": [
        {
            "id": 127110797,
            "links": {
                "accountabilities": [],
                "circle": 856843816,
                "domains": [],
                "people": [
                    911230097,
                    656753429,
                    1030470515
                ]
            },
            "name": "Developer",
            "purpose": null
        }
    ]
  },
  "projects": [
      {
          "id": 33867,
          "description": "Domain & Policy navigation storied out",
          "status": "Future",
          "waiting_on_who": "",
          "waiting_on_what": "",
          "link": null,
          "value": 5,
          "effort": 1,
          "roi": 5,
          "private_to_circle": false,
          "created_at": "2014-04-16T12:33:39Z",
          "links": {
              "role": 127110797,
              "person": 656753429,
              "circle": 856843816
          }
      }
  ]
```

#### Attribute Notes

  * **waiting_on_who**: only returned if status is waiting or status is future
  * **watiting_on_what**: only returned if status is waiting or status is future
  * **role**: when null, indicates Individual Action
  * **private_to_circle**: true indicates viewable only to circle members or admin

#### Security Note

**private_to_circle** projects should only be exposed to members of the projects' circle


Adding Projects (POST)
----------------------

### Create a Project

`curl -H "X-Auth-Token: $API_KEY" -X POST -d '{"projects":[{ "description":"API docs updated", "circle_id":346, "role_id":2331 }]}' https://glassfrog.holacracy.org/api/v3/projects`

A successful POST returns status 200 with the newly created resource in the body:

```
{
    "linked": {
        "circles": [
            {
                "id": 346,
                "links": {},
                "name": "GlassFrog",
                "short_name": "GlassFrog",
                "strategy": "Instill Holacracy Habits\r\n\r\nIntegration over Built-in Support\r\n\r\nSomething big each month"
            }
        ],
        "people": [],
        "roles": [
            {
                "id": 2331,
                "links": {
                    "circle": 346
                },
                "name": "Agile Process Coach",
                "purpose": "Implement, champion, and support agile software development practices"
            }
        ]
    },
    "projects": [
        {
            "created_at": "2014-08-07T15:05:44-04:00",
            "description": "API docs updated",
            "effort": null,
            "id": 51095,
            "link": null,
            "links": {
                "circle": 346,
                "person": null,
                "role": 2331
            },
            "private_to_circle": false,
            "roi": null,
            "status": "Current",
            "value": null
        }
    ]
}
```

#### Permissions Notes

API_keys from accounts with admin permissions can add projects to any circle in the organization.
Non admin accounts can only add projects to circles they are a member of.
Projects with the private_to_circle set to true can only be viewed by members of the circle the project added to.


#### Attributes

* **status** valid options for status are: "Current","Waiting","Future","Done","Archived"
* **roi** readonly field not specified on create, calculated from value / effort
* **description** and **waiting_on_who** fields support [role references](sections/people.md#role-references)



Updating Projects (PATCH/PUT)
---------------------------------


### Updating Description

`curl -H "X-Auth-Token: $API_KEY" -X PATCH -d '[{ "op":"replace","path":"/projects/0/description", "value":"Api Docs updated"}]' https://glassfrog.holacracy.org/api/v3/projects/$PROJECT_ID`

### Updating Multiple Attributes

`curl -H "X-Auth-Token: $API_KEY" -X PATCH -d '[{ "op":"replace","path":"/projects/0/description", "value":"More API doc changes"},{"op":"replace","path":"/projects/0/status", "value":"Future"}]' https://glassfrog.holacracy.org/api/v3/projects/$PROJECT_ID`

Returns 204 No Content on success.



Removing Projects
-------------------------------


### Archiving a Project (PATCH) update status to 'Archived'

`curl -H "X-Auth-Token: $API_KEY" -X PATCH -d '[{ "op":"replace","path":"/projects/0/status", "value":"Archived"}]' https://glassfrog.holacracy.org/api/v3/projects/$PROJECT_ID`

returns 204 No Content on success.

#### Archived projects are still accessible via their ID, but are not visible via UI or api project lists.


### Remove a Project completely (DELETE)

`curl -H "X-Auth-Token: $API_KEY" -X DELETE https://glassfrog.holacracy.org/api/v3/projects/$PROJECT_ID`

returns 204 No Content on success.

#### Deleted projects are removed from the database entirely.










