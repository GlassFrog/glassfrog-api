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
    "projects": {
        "created_at": "2014-05-27T15:08:41-04:00",
        "description": "A waiting project with cross referenced waiting on info",
        "id": 853879595,
        "links": {
            "circle": 856843816,
            "person": 911230097,
            "role": 127110797
        },
        "private_to_circle": false,
        "status": "Waiting",
        "waiting_on_what": "Report",
        "waiting_on_who": "@Business_Analyst"
    }
}
```

#### Attribute Notes

  * **waiting_on_who**: only returned if status is waiting or status is future
  * **watiting_on_what**: only returned if status is waiting or status is future
  * **role**: when null, indicates Individual Action
  * **private_to_circle**: true indicates viewable only to circle members or admin

#### Security Note

**private_to_circle** projects should only be exposed to members of the projects' circle









