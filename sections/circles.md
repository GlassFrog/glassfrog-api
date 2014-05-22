Circles
========


Getting circles
----------------

* `GET /circles` will return all circles in the organization.

Returns 200 OK with a response body in the following format when successful:

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


* `GET /circle.xml?include=members` will return all circles in the organization with a sublist of the members in each circle.

Returns 200 OK with a response body in the following format when successful:

```json
{
  "linked": {
    "members": [
      {
        "id": 657190835,
        "name": "Lawrence Copper",
        "email": "lawrence@fictional.com",
        "external_id": null
      },
      {
        "id": 811765527,
        "name": "Carlos Aldrich",
        "email": "carlos@fictional.com",
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

Getting circle roles
--------------------

* `GET /circle/[:id]/roles` will return all custom roles in the circle specified by [:id].

It can be used to map the structure of the whole organization by first finding the
circle ID of the Board circle from the method above,
using this method to list the roles in the Board circle,
and recursively traversing the circle structure using the supporting circle ID fields in the resulting role list.

Returns 200 OK with a response body in the following format when successful:


```json
{
  "linked": {
    "domains": [
      {
        "id": 1024896945,
        "description": "All records required of a Circle under the Constitution, and any record-keeping processes and systems required to create and maintain such records for the Circle."
      }
    ],
    "accountabilities": [
      {
        "id": 976665113,
        "description": "Facilitating the Circle’s Governance Meetings and Tactical Meetings in alignment with the rules of the Constitution, and enforcing such rules during such meetings as-needed"
      },
      {
        "id": 976665114,
        "description": "Auditing the meetings and records of the Circle’s Sub-Circles to assess alignment with the Constitution, including at a minimum whenever prompted to do so by the Rep Link from a Sub-Circle, and initiating the restorative process defined in the Constitution if a Process Breakdown is discovered within a Sub-Circle"
      },
      {
        "id": 976665065,
        "description": "Holding and energizing all Accountabilities of the Circle to the extent they have not been assigned to a Defined Role within the Circle"
      },
      {
        "id": 976665066,
        "description": "Assigning and removing Partners and other People to/from Defined Roles"
      },
      {
        "id": 976665067,
        "description": "Appointing People to serve as Circle Members of the Sub-Circle, and removing People from such appointments as-needed"
      },
      {
        "id": 976665068,
        "description": "Monitoring fit between the Sub-Circle’s Defined Roles and those Role-Fillers holding such Roles, and offering feedback and coaching to such Role-Fillers to enhance their capacity to express such Roles’ Purpose and enact such Roles’ Accountabilities"
      },
      {
        "id": 976665069,
        "description": "Allocating resources granted by the Super-Circle or otherwise acquired by the Sub-Circle across the various Projects, Roles, or Circle Members of the Sub-Circle, including as-desired assigning such allocation to such Roles and Circle Members or to the owners of such Projects"
      },
      {
        "id": 976665070,
        "description": "Defining priorities, strategies, and other guiding constraints on the Operational Process of the Sub-Circle, to align and integrate its work to better express its Purpose and Accountabilities, and to align with any priorities, strategy, or direction of its Super-Circle"
      },
      {
        "id": 976665071,
        "description": "Defining metrics which provide visibility into the Sub-Circle’s performance in expressing its Purpose, and assigning appropriate Roles of the Sub-Circle to collect data for each metric"
      },
      {
        "id": 976665079,
        "description": "Removing constraints that limit the Sub-Circle’s internal capacity to express its Purpose, but which fall outside of the Sub-Circle’s span of control or are otherwise beyond its capacity to resolve unless changes are made within its Super-Circle or to the other entities within such Super-Circle"
      },
      {
        "id": 976665080,
        "description": "Seeking to understand Tensions conveyed to the Rep Link by any of the Sub-Circle’s Circle Members, to identify those appropriate to process within the Super-Circle"
      },
      {
        "id": 976665081,
        "description": "Providing visibility to the Super-Circle into the health and sustainability of operations within the Sub-Circle"
      },
      {
        "id": 976665082,
        "description": "Defining metrics which provide visibility into the sustainability of the Sub-Circle’s capacity to produce results which express its Purpose, and assigning appropriate Roles of the Sub-Circle to collect data for each metric"
      },
      {
        "id": 976665095,
        "description": "Maintaining all records of a Circle required by the Constitution, including capturing the outputs of the Circle’s Governance Process and Tactical Meetings, maintaining a compiled view of all governance currently in effect for the Circle, and maintaining a list of all operational elements currently being monitored in Tactical Meetings"
      },
      {
        "id": 976665096,
        "description": "Scheduling all regular and special meetings of the Circle which are explicitly required by the Constitution or by a Policy established by the Circle, in alignment with the terms of the Constitution and any relevant Policies of the Circle, and notifying all Circle Members of times and locations for meetings so scheduled"
      },
      {
        "id": 976665097,
        "description": "Interpreting the acting governance of the Circle upon request of a Circle Member as provided for in the Constitution, including ruling on matters of due process, procedure, and authority related to or granted under such governance or the Constitution itself"
      }
    ],
    "circles": [
      {
        "id": 582240928,
        "name": "Operations",
        "short_name": "Ops",
        "strategy": "Emphasize \"Documenting & Aligning to Standards\", even over \"Developing & Co-Creating Novelty\"",
        "links": {
        }
      }
    ],
    "people": [
      {
        "id": 657190835,
        "name": "Lawrence Copper",
        "email": "lawrence@fictional.com",
        "external_id": null
      },
      {
        "id": 811765527,
        "name": "Carlos Aldrich",
        "email": "carlos@fictional.com",
        "external_id": null
      }
    ]
  },
  "roles": [
    {
      "id": 591359738,
      "name": "Facilitator",
      "purpose": "Circle governance and operational practices aligned with the core rules and processes of the Holacracy Constitution.",
      "elected_until": null,
      "links": {
        "domains": [

        ],
        "accountabilities": [
          976665113,
          976665114
        ],
        "circle": 582240928,
        "people": [

        ]
      }
    },
    {
      "id": 227315657,
      "name": "Lead Link",
      "purpose": "Supporting @Sales and @Development",
      "links": {
        "domains": [

        ],
        "accountabilities": [
          976665065,
          976665066,
          976665067,
          976665068,
          976665069,
          976665070,
          976665071
        ],
        "circle": 582240928,
        "people": [
          657190835
        ]
      }
    },
    {
      "id": 1067657170,
      "name": "Rep Link",
      "purpose": "Tensions relevant to process in the Super-Circle channeled out and resolved.",
      "elected_until": null,
      "links": {
        "domains": [

        ],
        "accountabilities": [
          976665079,
          976665080,
          976665081,
          976665082
        ],
        "circle": 582240928,
        "people": [

        ]
      }
    },
    {
      "id": 959905549,
      "name": "Secretary",
      "purpose": "Stabilize the Circle's governance over time as a steward of the Circle's formal records and record-keeping process.",
      "elected_until": null,
      "links": {
        "domains": [
          1024896945
        ],
        "accountabilities": [
          976665095,
          976665096,
          976665097
        ],
        "circle": 582240928,
        "people": [
          657190835
        ]
      }
    },
    {
      "id": 629795917,
      "name": "Apos'trophe",
      "purpose": null,
      "links": {
        "domains": [

        ],
        "accountabilities": [

        ],
        "circle": 582240928,
        "people": [
          657190835
        ]
      }
    },
    {
      "id": 83866836,
      "name": "Crosslink Role",
      "purpose": null,
      "links": {
        "domains": [

        ],
        "accountabilities": [

        ],
        "circle": 582240928,
        "people": [
          811765527
        ]
      }
    }
  ]
}```
