Projects
==========

Retrieving Projects (GET)
--------------------------

#### Response Format

```json
"linked": {
    "circles": [
        {
            "id": 856843816,
            "links": {},
            "name": "Development",
            "shortName": "DDC",
            "strategy": "Emphasize \"Working Software\", even over \"Comprehensive Documentation\""
        }
    ],
    "people": [
        {
            "email": "monica@example.com",
            "externalId": null,
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
        "createdAt": "2014-05-27T15:08:41-04:00",
        "description": "A waiting project with cross referenced waiting on info",
        "id": 853879595,
        "links": {
            "circle": 856843816,
            "person": 911230097,
            "role": 127110797
        },
        "privateToCircle": false,
        "status": "Waiting",
        "waitingOnWhat": "Report",
        "waitingOnWho": "@Business_Analyst"
    }
}
```

### Getting all Projects on a Circle

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles/$CIRCLE_ID/projects`

OR

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/projects?circle_id=$CIRCLE_ID`


#### Attribute Notes

  * **waiting_on_who**: only returned if status is waiting or status is future
  * **watiting_on_what**: only returned if status is waiting or status is future
  * **role**: when null, indicates Individual Action
  * **private_to_circle**: true indicates viewable only to circle members or admin

#### Security Note

*private_to_circle*: projects should only be exposed to members of the projects' circle









