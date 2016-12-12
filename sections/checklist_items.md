Checklist Items
==========

Retrieving Checklist Items (GET)
--------------------------

### Getting all Checklist Items on a Circle (including global items)

`curl -H "X-Auth-Token: $API_KEY" https://api.glassfrog.com/api/v3/circles/$CIRCLE_ID/checklist_items`

OR

`curl -H "X-Auth-Token: $API_KEY" https://api.glassfrog.com/api/v3/checklist_items?circle_id=$CIRCLE_ID`


### Getting all Checklist Items on a Circle without global items

`curl -H "X-Auth-Token: $API_KEY" 'https://api.glassfrog.com/api/v3/checklist_items?circle_id=856843816&global=false'`

### Getting all Global Checklist Items

`curl -H "X-Auth-Token: $API_KEY" https://api.glassfrog.com/api/v3/checklist_items?global=true`


#### Response Format

```json
{
    "checklist_items": [
        {
            "description": "A Global Checklist item on Facilitators",
            "frequency": "Weekly",
            "global": true,
            "id": 35243513,
            "link": "http://example.com",
            "links": {
                "circle": null,
                "role": null
            },
            "role_name": "Facilitator"
        },
        {
            "description": "Everyone checklist item from fixtures",
            "frequency": "Monthly",
            "global": false,
            "id": 688606235,
            "link": null,
            "links": {
                "circle": 856843816,
                "role": null
            }
        },
        {
            "description": "Global Checklist Item for Some Company",
            "frequency": "Quarterly",
            "global": true,
            "id": 434414356,
            "link": null,
            "links": {
                "circle": null,
                "role": null
            },
            "role_name": null
        }
    ],
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
        "roles": [
            {
                "id": 905502603,
                "links": {},
                "name": "Principal Developer",
                "purpose": null
            },
            {
                "id": 983551267,
                "links": {},
                "name": "Business Analyst",
                "purpose": null
            }
        ]
    }
}
```

#### Attribute Notes

* **role**:  role of 'Circle Member' indicates checklist item applies to all circle members.
* **frequency**: frequency of the item; allowed values are 'Weekly', 'Monthly', and 'Quarterly'
* **global**: indicates a global item that will show up on each circle for 'All Circle Members' in the organization.
* **role_name**: Core Role name (Lead Link, Rep Link, Facilitator, Secretary) only if 'global' is true; indicates global item will show up on each circle for that role

#### Permissions Notes

Admin permissions are required to create global items.
Lead link, secretary, or rep link can create items for the whole circle.
Other circle members may create items for any role they fill.


Adding Checklist Items (POST)
-------------------------------

### Create a Checklist Item

`curl -H "X-Auth-Token: $API_KEY" -X POST -d '{"checklist_items":[{"description":"A New Item", "frequency":"Weekly", "circle_id":856843816, "role_id":905502603}]}' https://api.glassfrog.com/api/v3/checklist_items`

A successful POST returns status 200 with the newly created resource in the body:

```
{
    "checklist_items": [
        {
            "description": "A New Item",
            "frequency": "Weekly",
            "global": false,
            "id": 975931263,
            "link": null,
            "links": {
                "circle": 856843816,
                "role": 905502603
            }
        }
    ],
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
        "roles": [
            {
                "id": 905502603,
                "links": {},
                "name": "Principal Developer",
                "purpose": null
            }
        ]
    }
}
```


#### Attribute Notes

* **role_id** set to null to create a Checklist Item for all circle members.

Updating Checklist Items (PATCH)
-------------------------------

### Updating Description

`curl -H "X-Auth-Token: $API_KEY" -X PATCH -d '[{ "op":"replace","path":"/checklist_items/0/description", "value":"Api Docs updated"}]' https://api.glassfrog.com/api/v3/checklist_items/$CHECKLIST_ITEM_ID`

### Updating Multiple Attributes

`curl -H "X-Auth-Token: $API_KEY" -X PATCH -d '[{ "op":"replace","path":"/checklist_items/0/description", "value":"Update API Docs"},{"op":"replace","path":"/checklist_items/0/frequency", "value":"Monthly"}]' https://api.glassfrog.com/api/v3/checklist_items/$CHECKLIST_ITEM_ID`

Returns 204 No Content on success.


Removing Checklist Items
-------------------------------

### Remove a Checklist Item (DELETE)

`curl -H "X-Auth-Token: $API_KEY" -X DELETE https://api.glassfrog.com/api/v3/checklist_items/$CHECKLIST_ITEM_ID`

returns 204 No Content on success.
