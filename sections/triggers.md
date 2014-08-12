Triggers
========

Retrieving Triggers (GET)
----------------------

#### Filtering by person_id

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/triggers?person_id=$PERSON_ID`

#### Filtering by circle_id

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/triggers?circle_id=$CIRCLE_ID`

#### Filtering by created_since

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/triggers?create_since=$ISO8601_DATE`

Dates should be specified in iso8601 format ie. 2007-04-05T12:30-02:00
If the date string does not specify a timezone (ie. 2007-04-05), GlassFrog assumes UTC.


#### Response Format

```json
{
    "linked": {
        "roles": [
            {
                "id": 22017,
                "name": "Cross Link from HolacracyOne Service Delivery",
                "purpose": "[HolacracyOne Service Delivery's Purpose]",
                "links": {}
            }
        ],
        "people": [
            {
                "id": 52,
                "name": "Tom Thomison",
                "email": "tom@example.com",
                "external_id": null
            }
        ],
        "circles": [
            {
                "id": 1506,
                "name": "Holacracy Group",
                "short_name": "Holacracy Group",
                "strategy": "<i>Emphasize:</i>\r\n\r\n• Strategy <i>over</i> Logistics, Logistics <i>over</i> Tactics\r\n\r\n• Helping Holacracy outgrow HolacracyOne and stand alone <i>even over</i> Leveraging Holacracy for HolacracyOne\r\n",
                "links": {}
            }
        ]
    },
    "triggers": [
        {
            "id": 480,
            "description": "Send to Bernard Marie",
            "private_to_circle": false,
            "created_at": "2014-07-31T16:01:40Z",
            "links": {
                "role": 22017,
                "person": 52,
                "circle": 1506
            }
        }
    ]
}
```
