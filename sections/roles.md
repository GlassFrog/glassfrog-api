Roles
========

Retrieving roles (GET)
----------------------

#### response format

```json
{
  "linked": {
    "circles": [
      {
        "id": 582240928,
        "name": "Operations",
        "shortName": "Ops",
        "strategy": "Emphasize \"Documenting & Aligning to Standards\", even over \"Developing & Co-Creating Novelty\"",
        "links": {
        }
      }
    ],
    "people": [
      {
        "id": 811765527,
        "name": "Carlos Aldrich",
        "email": "carlos@example.com",
        "externalId": null
      }
    ]
  },
  "roles": [
    {
      "id": 83866836,
      "name": "Fulfillment Role",
      "purpose": null,
      "links": {
        "domains": [],
        "accountabilities": [],
        "circle": 582240928,
        "people": [
          811765527
        ]
      }
    }
  ]
}
```

###### Notes

* Elected roles will also include elected_until attribute, which returns the end date for current term.


### Get all Roles for Organization

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/roles`

### Get a specific Role

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/roles/$ROLE_ID`


### Filtering by Person

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/roles?person_id=$PERSON_ID`

OR

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/people/$PERSON_ID/roles`

returns roles for a particular person:


### Filtering by Circle

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/roles?circle_id=$CIRCLE_ID`

OR

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/circles/$CIRCLE_ID/roles`


Updating Role Assignments ( PUT / PATCH )
-----------------------------------

With the exception of Lead Link roles, role assignment is additive and will add new role-fillers. Assigning Lead Links is special case, see below for more details.

### adding a role assignment

`curl -H "X-Auth-Token: $API_KEY" -X PATCH -d '[{"op":"add","path":"/roles/0/links/people/$PERSON_ID"}]' https://glassfrog.holacracy.org/api/v3/roles/$ROLE_ID`

### removing role assignment

`curl -H "X-Auth-Token: $API_KEY" -X PATCH -d '[{"op":"remove","path":"/roles/0/links/people/$PERSON_ID"}]' https://glassfrog.holacracy.org/api/v3/roles/$ROLE_ID`

#### Emails sent:

Assigning roles via the API *will* send email notifications to added and removed role-fillers.

#### assigning Lead Links

To assign to the Lead Link of a circle, you must assign to the corresponding role in the super-circle; you can't assign directly to the Lead Link role of a circle.
Additionally, this role is always single filled, and assigning it will replace the current role-filler rather than adding a new
role-filler. In the case of a successful replacement, the API will return 200 and the role, otherwise if there is no previous
role-filler that is replaced, it will return 204.






