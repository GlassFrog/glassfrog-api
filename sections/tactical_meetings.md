Tactical Meetings
=================

Retrieving Tactical Meetings (GET)
----------------------------------

### Get all Tactical Meetings in the Organization's History

`curl -H "X-Auth-Token: $API_KEY" https://api.glassfrog.com/api/v3/tactical_meetings`

### Get a Specific Tactical Meeting

`curl -H "X-Auth-Token: $API_KEY" https://api.glassfrog.com/api/v3/tactical_meetings/$TACTICAL_MEETING_ID`

#### Response Format

```json
{
  "linked": {
    "circles": [
      {
        "id": 25,
        "name": "General Company Circle",
        "short_name": "GCC",
        "strategy": "<i>Focus On:</i>\r\n\r\n• Build & Support the \"Whole Product\"\r\n\r\n• Support Behavior Change\r\n",
        "links": {
          "roles": [
          ],
          "policies": [
          ],
          "domain": [
          ],
          "supported_role": {
            "id": 136,
            "name": "General Company Circle",
            "purpose": "Exquisite Organization",
            "links": {
              "domains": [
                847,
                7646
              ],
              "accountabilities": [
                13208,
                27591,
                27592,
                145568
              ],
              "circle": 16,
              "supporting_circle": 25,
              "people": [
                47
              ]
            }
          }
        }
      }
    ],
    "people": [
      {
        "id": 916,
        "name": "Olivier Compagne",
        "email": "olivier@holacracyone.com",
        "external_id": null,
        "links": {}
      }
    ],
    "agenda_items": [
      {
        "id": 62360,
        "label": null,
        "completed": true,
        "position": 3,
        "person_id": null,
        "meeting_id": 20114,
        "tension_id": null,
        "proposal_id": null,
        "links": {
          "tension": null,
          "proposal": null,
          "person": null
        }
      },
      {
        "id": 62361,
        "label": null,
        "completed": true,
        "position": 4,
        "person_id": null,
        "meeting_id": 20114,
        "tension_id": null,
        "proposal_id": null,
        "links": {
          "tension": null,
          "proposal": null,
          "person": null
        }
      },
      {
        "id": 62362,
        "label": null,
        "completed": true,
        "position": 5,
        "person_id": null,
        "meeting_id": 20114,
        "tension_id": null,
        "proposal_id": null,
        "links": {
          "tension": null,
          "proposal": null,
          "person": null
        }
      }
    ]
  },
  "tactical_meetings": [
    {
      "id": 20114,
      "started_at": "2014-04-04T21:20:57+02:00",
      "ended_at": "2014-04-04T22:22:28+02:00",
      "links": {
        "circle": 25,
        "owner": 916,
        "agenda_items": [
          62360,
          62361,
          62362
        ]
      }
    }
  ]
}
```


Updating Tactical Meetings (PATCH/PUT)
--------------------------------------


### Updating Multiple Attributes

`curl -H "X-Auth-Token: $API_KEY" -X PATCH -d '[
  { "op":"replace","path":"/tactical_meetings/0/person_id", "value":"123"},
  { "op":"replace","path":"/tactical_meetings/0/current_agenda_item_id", "value":"456"}
]' https://api.glassfrog.com/api/v3/tactical_meetings/$TACTICAL_MEETING_ID`

Returns 204 No Content on success.


