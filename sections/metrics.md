Metrics
==========

Retrieving Metrics (GET)
--------------------------

### Getting all Metrics on a Circle (including global metrics)

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles/$CIRCLE_ID/metrics`

OR

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/metrics?circle_id=$CIRCLE_ID`


### Getting all Metrics on a Circle without global metrics

`curl -H "X-Auth-Token: $API_KEY" 'https://glassfrog.holacracy.org/api/v3/metrics?circle_id=856843816&global=false'`

### Getting all Global Metrics

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/metrics?global=true`


#### Response Format

```json
{
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
    },
    "metrics": [
        {
            "description": "Test metric from fixtures",
            "frequency": "Weekly",
            "global": false,
            "id": 783472353,
            "link": "http://example.com/",
            "links": {
                "circle": 856843816,
                "role": 905502603
            }
        },
        {
            "description": "A Global Metric",
            "frequency": "Weekly",
            "global": true,
            "id": 186949289,
            "link": "http://example.com/",
            "links": {
                "circle": null,
                "role": null
            },
            "role_name": null
        },
        {
            "description": "A Global Metric for Facilitators",
            "frequency": "Weekly",
            "global": true,
            "id": 627727933,
            "link": "http://example.com/",
            "links": {
                "circle": null,
                "role": null
            },
            "role_name": "Facilitator"
        }
    ]
}```

#### Attribute Notes

* **frequency**: frequency of the metrics; allowed values are 'Weekly', 'Monthly', and 'Quarterly'
* **global**: indicates a global metric that will show up on each circle for 'All Circle Members' in the organization.
* **role_name**: Core Role name (Lead Link, Rep Link, Facilitator, Secretary) only if 'global' is true; indicates global metric will show up on each circle for that role

#### Permissions Notes

Admin permissions are required to create global metrics.
Other circle members may create metrics for any role they fill.


Adding Metrics (POST)
-------------------------------

### Create a Metric

`curl -H "X-Auth-Token: $API_KEY" -X POST -d '{"metrics":[{"description":"A New Metric", "frequency":"Weekly", "circle_id":856843816, "role_id":905502603}]}' https://glassfrog.holacracy.org/api/v3/metrics`

A successful POST returns status 200 with the newly created resource in the body:

```
{
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
    },
    "metrics": [
        {
            "description": "A New Metric",
            "frequency": "Weekly",
            "global": false,
            "id": 783472354,
            "link": null,
            "links": {
                "circle": 856843816,
                "role": 905502603
            }
        }
    ]
}
```


Updating Metrics (PATCH)
-------------------------------

### Updating Description

`curl -H "X-Auth-Token: $API_KEY" -X PATCH -d '[{ "op":"replace","path":"/metrics/0/description", "value":"number of Api Doc changes"}]' https://glassfrog.holacracy.org/api/v3/metrics/$METRIC_ID`

### Updating Multiple Attributes

`curl -H "X-Auth-Token: $API_KEY" -X PATCH -d '[{ "op":"replace","path":"/metrics/0/description", "value":"number of Api Doc changes"},{"op":"replace","path":"/metrics/0/frequency", "value":"Monthly"}]' https://glassfrog.holacracy.org/api/v3/metrics/$METRIC_ID`

Returns 204 No Content on success.


Removing Metrics
-------------------------------

### Remove a Metric (DELETE)

`curl -H "X-Auth-Token: $API_KEY" -X DELETE https://glassfrog.holacracy.org/api/v3/metrics/$METRIC_ID`

returns 204 No Content on success.
