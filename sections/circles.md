Circles
========

Getting all circles in the organization
----------------

`curl -H "X-Auth-Token: $API_KEY" https://nexus-staging.holacracy.org/api/v3/circles`

will return all circles in the organization:

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


Getting all circles and members in the organization
----------------

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



Shortcuts
----------------
* /people
* /roles
* /projects
* /metrics
* /checklist_items
