Checklist Items
==========

Retrieving Checklist Items (GET)
--------------------------

### Getting all Checklist Items on a Circle

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles/$CIRCLE_ID/checklist_items`

OR

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/checklist_items?circle_id=$CIRCLE_ID`


#### Response Format

```json
{
    "checklist_items": [
        {
            "description": "Test checklist item from fixtures",
            "frequency": "Weekly",
            "id": 589485761,
            "link": "https://www.somewhere.com/",
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
                "links": {
                    "accountabilities": [ ],
                    "circle": 856843816,
                    "domains": [],
                    "people": [
                        516784585
                    ]
                },
                "name": "Principal Developer",
                "purpose": null
            }
        ]
    }
}
```

#### Attribute Notes

* **role**:  role of 'Circle Member' indicates checklist item applies to all circle members.





