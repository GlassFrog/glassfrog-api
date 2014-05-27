Metrics
==========

Retrieving Metrics (GET)
--------------------------

#### Response Format

```json
{
    "metrics": [
        {
            "description": "Test metric from fixtures",
            "frequency": "Weekly",
            "id": 783472353,
            "link": "https://glassfrog.holacracy.org/",
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
                "shortName": "DDC",
                "strategy": "Emphasize \"Working Software\", even over \"Comprehensive Documentation\""
            }
        ],
        "roles": [
            {
                "id": 905502603,
                "links": {
                    "accountabilities": [],
                    "circle": 856843816,
                    "domains": [],
                    "people": []
                },
                "name": "Principal Developer",
                "purpose": null
            }
        ]
    }
}
```

### Getting all Metrics on a Circle

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles/$CIRCLE_ID/metrics`

OR

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/metrics?circle_id=$CIRCLE_ID`







