Actions
========

Retrieving Actions (GET)
----------------------

#### Filtering by person_id

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/actions?person_id=$PERSON_ID`

#### Filtering by circle_id

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/actions?circle_id=$CIRCLE_ID`

#### Filtering by created_since

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/actions?created_since=$ISO8601_DATE`

Dates should be specified in iso8601 format ie. 2007-04-05T12:30-02:00
If the date string does not specify a timezone (ie. 2007-04-05), GlassFrog assumes UTC.


#### Response Format

```json
{
    "linked": {
        "roles": [
            {
                "id": 1872,
                "name": "Training Operations",
                "purpose": "Flowing logistics for great experiences",
                "links": {}
            }
        ],
        "people": [
            {
                "id": 914,
                "name": "Karilen Mays",
                "email": "karilen@example.com",
                "external_id": null
            }
        ],
        "circles": [
            {
                "id": 353,
                "name": "HolacracyOne Service Delivery",
                "short_name": "Service Delivery",
                "strategy": "<i>Emphasize:</i>\r\n\r\nReducing early engagement turbulence <i>even over</i> Optimizing elsewhere\r\n\r\nDistilling and structuring knowledge for reuse <i>even over</i> Entrepreneurial zeal",
                "links": {}
            }
        ]
    },
    "actions": [
        {
            "id": 78591,
            "description": "Talk to Sabrina about reception for PCT",
            "private_to_circle": false,
            "created_at": "2014-07-31T20:27:20Z",
            "links": {
                "role": 1872,
                "person": 914,
                "circle": 353
            }
        }
    ]
}
```
