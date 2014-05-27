Circles
========

Retrieving Circles (GET)
----------------------

#### Response Format

```json
{
  "circles": [
    {
      "id": 429327429,
      "name": "Board",
      "short_name": "Board",
      "strategy": null,
      "links": {
      }
    },
    {
      "id": 1041583805,
      "name": "GCC",
      "short_name": "GCC",
      "strategy": "Emphasize \"Documenting & Aligning to Standards\", even over \"Developing & Co-Creating Novelty\"",
      "links": {
      }
    },
  ]
}
```

### A Specific Circle

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles/$CIRCLE_ID`


### All Circles in the Organization

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles`



### Including Members in the Response (include=members)

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles?include=members`

will return all circles in the organization with a sublist of the members in each circle:

```json
{
  "linked": {
    "people": [
      {
        "id": 657190835,
        "name": "Lawrence Copper",
        "email": "lawrence@example.com",
        "external_id": null
      },
      {
        "id": 811765527,
        "name": "Carlos Aldrich",
        "email": "carlos@example.com",
        "external_id": null
      },
    ]
  },
  "circles": [
    {
      "id": 582240928,
      "name": "Operations",
      "short_name": "Ops",
      "strategy": "Emphasize \"Documenting & Aligning to Standards\", even over \"Developing & Co-Creating Novelty\"",
      "links": {
        "people": [
          811765527,
          657190835
        ]
      }
    }
  ]
}
```


Aliases
----------------

The circles endpoint also supports aliases that refer to the following resources for a specific circle. See the documentation for
  each resource below for options:

##### [People](/people.md)

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles/$CIRCLE_ID/people`

##### [Roles](/roles.md)

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles/$CIRCLE_ID/roles`

##### [Projects](/projects.md)

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles/$CIRCLE_ID/projects`

##### [Metrics](/metrics.md)

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles/$CIRCLE_ID/metrics`

##### [Checklist Items](/checklist_items.md)

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles/$CIRCLE_ID/checklist_items`
