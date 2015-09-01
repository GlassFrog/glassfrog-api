Tactical Meetings
=================

[:show, :index, :update]
------------------------

Retrieving Tactical Meetings (GET)
----------------------------------

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/tactical_meetings`

`curl -H "X-Auth-Token: $API_KEY" https://glassfrog.holacracy.org/api/v3/tactical_meetings/$TACTICAL_MEETING_ID`

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
            {
              "id": 73328,
              "name": "2nd Signer",
              "purpose": "Prevent fraudulent transfers",
              "links": {
                "domains": [],
                "accountabilities": [
                  298958
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  914
                ]
              }
            },
            {
              "id": 3259,
              "name": "Bookkeeper",
              "purpose": "Process transactions with clarity & coherence; guard the books from chaos",
              "links": {
                "domains": [],
                "accountabilities": [
                  6466,
                  6467,
                  6468,
                  45973,
                  45974,
                  68995
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  13935
                ]
              }
            },
            {
              "id": 54138,
              "name": "Bookkeeper Liaison",
              "purpose": "",
              "links": {
                "domains": [],
                "accountabilities": [
                  205274,
                  205275,
                  205276,
                  205277,
                  205278,
                  205279
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  10480,
                  914
                ]
              }
            },
            {
              "id": 1311,
              "name": "Brand Protection",
              "purpose": "Protect the integrity of HolacracyOne’s brands",
              "links": {
                "domains": [],
                "accountabilities": [
                  13682,
                  13683,
                  138929
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  916
                ]
              }
            },
            {
              "id": 73327,
              "name": "Check Depositor",
              "purpose": "Checks deposited and recorded, immediately and accurately",
              "links": {
                "domains": [],
                "accountabilities": [
                  298957
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  914
                ]
              }
            },
            {
              "id": 59395,
              "name": "Collection Steward",
              "purpose": "Money owed = money paid",
              "links": {
                "domains": [],
                "accountabilities": [
                  236570,
                  236571
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  10480,
                  914
                ]
              }
            },
            {
              "id": 9466,
              "name": "Constitution Steward",
              "purpose": "The Holacracy Constitution; legally-grounded, projection-free, & continually-evolving",
              "links": {
                "domains": [
                  3564
                ],
                "accountabilities": [
                  37445,
                  37446,
                  37447
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  47
                ]
              }
            },
            {
              "id": 34799,
              "name": "Design Services",
              "purpose": "Awesome design, as a service",
              "links": {
                "domains": [],
                "accountabilities": [
                  117719,
                  117720,
                  117721,
                  117816
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  14447
                ]
              }
            },
            {
              "id": 76973,
              "name": "DIY Support",
              "purpose": "Boost the odds that Do-It-Yourself Holacracy adoption succeeds",
              "links": {
                "domains": [
                  107886
                ],
                "accountabilities": [
                  317917,
                  317918,
                  317919,
                  317920,
                  317921,
                  317922
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  9497
                ]
              }
            },
            {
              "id": 140,
              "name": "Facilitator",
              "purpose": "Circle governance and operational practices aligned with the Constitution.",
              "elected_until": "2016-02-26",
              "links": {
                "domains": [],
                "accountabilities": [
                  34132,
                  34133
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  914
                ]
              }
            },
            {
              "id": 207,
              "name": "Finance",
              "purpose": "Be a good steward of the organization’s finances – minimize waste and maximize stability.",
              "links": {
                "domains": [
                  400,
                  398
                ],
                "accountabilities": [
                  1797,
                  6469,
                  6470,
                  6471,
                  21819,
                  52474
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  47
                ]
              }
            },
            {
              "id": 12793,
              "name": "Fulfillment Falcon",
              "purpose": "Flawless fulfillment",
              "links": {
                "domains": [],
                "accountabilities": [
                  57927,
                  57928,
                  57929,
                  57930,
                  57931,
                  65763,
                  85752
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  10480
                ]
              }
            },
            {
              "id": 3676,
              "name": "GlassFrog",
              "purpose": "Make Holacracy easier and more powerful through software",
              "links": {
                "domains": [
                  865297,
                  846,
                  29619,
                  58801,
                  58800
                ],
                "accountabilities": [
                  11062,
                  28046,
                  28049,
                  68996,
                  98643
                ],
                "circle": 25,
                "supporting_circle": 346,
                "people": [
                  53
                ]
              }
            },
            {
              "id": 1334955,
              "name": "Holacracy Coaching Facilitator",
              "purpose": "To model and coach Holacracy Practice internally during meetings",
              "links": {
                "domains": [],
                "accountabilities": [
                  1635695,
                  1635696
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  14447,
                  916
                ]
              }
            },
            {
              "id": 17283,
              "name": "Holacracy Ecosystem",
              "purpose": "A strong ecosystem of Holacracy practitioners, coaches, and licensees, learning together and supporting each other",
              "links": {
                "domains": [
                  107887,
                  62733,
                  6415
                ],
                "accountabilities": [
                  56929,
                  68999,
                  76389,
                  100964,
                  205290,
                  205291,
                  211437,
                  308680,
                  317923
                ],
                "circle": 25,
                "supporting_circle": 1506,
                "people": [
                  916
                ]
              }
            },
            {
              "id": 429,
              "name": "HolacracyOne Service Delivery",
              "purpose": "Help organizations implement Holacracy and the people within leverage it",
              "links": {
                "domains": [
                  58826,
                  65,
                  6413
                ],
                "accountabilities": [
                  738,
                  898,
                  1792,
                  15740,
                  98642
                ],
                "circle": 25,
                "supporting_circle": 353,
                "people": [
                  914
                ]
              }
            },
            {
              "id": 138,
              "name": "Lead Link",
              "purpose": "Exquisite Organization",
              "links": {
                "domains": [
                  2869
                ],
                "accountabilities": [
                  29631,
                  29632,
                  29633,
                  29634,
                  29635
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  47
                ]
              }
            },
            {
              "id": 208,
              "name": "Legal",
              "purpose": "Capture abstract intended agreements into concretely-defined relationships.",
              "links": {
                "domains": [
                  17,
                  16
                ],
                "accountabilities": [
                  268,
                  981,
                  6717,
                  76393
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  47
                ]
              }
            },
            {
              "id": 4466,
              "name": "Licensing Design",
              "purpose": "A sustainable & effective framework for licensing",
              "links": {
                "domains": [
                  2695,
                  1105,
                  1106
                ],
                "accountabilities": [
                  13673,
                  13675,
                  28748
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  47
                ]
              }
            },
            {
              "id": 2840,
              "name": "Outreach",
              "purpose": "Authentically attract to the Holacracy brand, and connect people into Holacracy products and services",
              "links": {
                "domains": [
                  88108,
                  319,
                  29618,
                  317,
                  91310,
                  363
                ],
                "accountabilities": [
                  5770,
                  11136,
                  15738,
                  21818,
                  145068,
                  177113,
                  205270,
                  277339,
                  277340,
                  277342,
                  1105335,
                  1265956
                ],
                "circle": 25,
                "supporting_circle": 285,
                "people": [
                  9497
                ]
              }
            },
            {
              "id": 28826,
              "name": "People & Partnership",
              "purpose": "Healthy partners, healthy tribe, healthy collisions",
              "links": {
                "domains": [
                  1024534,
                  11375,
                  10739
                ],
                "accountabilities": [
                  93118,
                  93119,
                  93120,
                  98770,
                  98771,
                  127591,
                  127592,
                  1265955
                ],
                "circle": 25,
                "supporting_circle": 2432,
                "people": [
                  47
                ]
              }
            },
            {
              "id": 30970,
              "name": "Pricing Strategy",
              "purpose": "Cohesive valuing and pricing of packaged company services",
              "links": {
                "domains": [],
                "accountabilities": [
                  98644,
                  98645
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  47
                ]
              }
            },
            {
              "id": 142,
              "name": "Rep Link",
              "purpose": "Tensions relevant to process in the Super-Circle channeled out and resolved.",
              "elected_until": "2017-03-24",
              "links": {
                "domains": [],
                "accountabilities": [
                  31592,
                  31593,
                  31594
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  914
                ]
              }
            },
            {
              "id": 139,
              "name": "Secretary",
              "purpose": "Steward and stabilize the Circle’s formal records and record-keeping process.",
              "elected_until": "2017-03-24",
              "links": {
                "domains": [
                  514
                ],
                "accountabilities": [
                  32837,
                  32838,
                  32839
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  47
                ]
              }
            },
            {
              "id": 40762,
              "name": "Tracker Tracker",
              "purpose": "Trustworthy tracking systems",
              "links": {
                "domains": [],
                "accountabilities": [
                  145108,
                  145109
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  14447
                ]
              }
            },
            {
              "id": 973228,
              "name": "Zen Master",
              "purpose": "Effective core logistics for help desk support platform",
              "links": {
                "domains": [
                  1023703
                ],
                "accountabilities": [
                  1265118,
                  1265119
                ],
                "circle": 25,
                "supporting_circle": null,
                "people": [
                  14447
                ]
              }
            }
          ],
          "policies": [
            {
              "id": 1000,
              "title": "Advances for Membership Requirements",
              "body": "Any Partner of HolacracyOne may take an advance against future partnership distributions solely for the purpose of funding necessary purchases to meet the requirements of membership in the Organization. Such advance shall be limited to a maximum of one advance per calendar year and an advanced amount not to exceed 60% of such member’s monthly draw, or, if such draw is documented to be higher in the fourth month following the date of such draw, then 60% of such higher draw amount. HolacracyOne shall reclaim any amounts so advanced by deducting the amount of such advance from such member’s monthly draw in three equal monthly installments beginning with the draw issued in the fourth month following the month in which such advance was taken. Notwithstanding the foregoing, no advance shall be allowed to cross a calendar-year boundary, and thus HolacracyOne shall reclaim the full amount of any remaining outstanding advances from the last draw issued during a calendar year.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": 847
              }
            },
            {
              "id": 264,
              "title": "Applying Travel Policies",
              "body": "All client contracts shall allow application of H1's Travel policies.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 147,
              "title": "Approved Billing Models",
              "body": "Any role entering into a financial relationship with clients shall use a billing model approved by Finance, or track and administer the transactions themselves in a manner that translates anything sent to Finance into an approved model.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 3628,
              "title": "Attention Point System",
              "body": "This policy defines a new type of currency for the organization, called \"Attention Points\" (or AP's for short).  Attention Points will ultimately get allocated to a role, to \"fund\" the role with partner attention.  A role allocated 100 Attention Points indicates the ideal attention for that role equals one full-focus partner in total; 200 AP's means the ideal attention is that of two full-focus partners, while 50 means the ideal is half of a full-focus partner's attention.\r\n\r\nNo partner may dedicate more focus to a role on a sustained, ongoing basis than is called for by the allocated Attention Points.  Further, if a partner has more than his/her full-focus worth of role assignments in total, the number of AP's associated with each assignment should be interpreted as a rough relative prioritization for how to split attention across roles; however, any conflicting prioritizations shall overrule this one (e.g. explicit prioritizations given by a relevant Lead Link or other prioritization role/system).  For the purpose of these calculations, if a role is multi-filled, the Attention Points allocated to the role are considered to be evenly divided across the role-fillers, unless otherwise specified by whomever assigns people into that role.\r\n\r\nOnly the Lead Link of the circle adopting this policy may create new Attention Points, and once created they become a resource of the circle, similar to a cash budget.  The partner or role that owns/controls Attention Points may allocate them to a role to fund desired attention within the role, or may transfer them to another partner or role to so allocate.  Once allocated to a role/circle, Attention Points may be unallocated and reallocated by whatever role/partner allocated them in the first place.\r\n\r\nIn addition to allocating a specific number of Attention Points to a role, anyone controlling AP's may also allow a role-filler to self-allocate AP's to the role from the funder's budget, within any constraints desired.  For example, a Lead Link might specify an allocation of \"Whatever is Needed\" on a role providing a key support function, and tell the role-filler to self-allocate as many AP's as he/she needs to get enough attention in the role to prevent critical work from dropping (these AP's would still come from the Circle's supply, they would just get allocated by the role-filler based on experience, rather than by the Lead Link based on an intended funding level).",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 1976,
              "title": "Certification Requirements for Delivery",
              "body": "No one may deliver Holacracy-branded services without a current Holacracy certification.  Those with a Holacracy certification may do so only when licensed to do so personally or when acting on behalf of a licensed entity.  The following further restrictions per certification level must also be honored (capitalized terms have the definition given in the most current licensing contract published by @Licensing_Design):\n\nCertified Holacracy Practitioner\n\nIf your highest level of Holacracy certification is “Certified Holacracy Practitioner”:\n•\tYou may only deliver Licensed Events that are presentations of 2 hours or less, and that do not include any live meeting simulations or similar demonstrations.  You may not claim such events are teaching skills or otherwise building or resulting in skills for the use or application of Holacracy.\n•\tYou may only deliver Holacracy-branded events using a standard event design published by HolacracyOne.  You may not make any significant changes to this design or any materials used in delivery, unless approval is explicitly granted by a relevant role in HolacracyOne.\n•\tYou may not deliver Licensed Discovery Sessions, except in an assisting capacity when an authorized person is leading the delivery.\n•\tYou may not sell or deliver Licensed Services whatsoever.\n\nCertified Holacracy Facilitator\n\nIf your highest level of Holacracy certification is “Certified Holacracy Facilitator”:\n•\tYou may only deliver Licensed Events of up to 8 hours; they may include live meeting simulations or similar demonstrations.  You may not claim such events are teaching skills or otherwise building or resulting in skills for the use or application of Holacracy.\n•\tYou may only deliver Holacracy-branded events using a standard event design published by HolacracyOne.  You may not make any significant changes to this design or any materials used in delivery, unless approval is explicitly granted by a relevant role in HolacracyOne.\n•\tYou may only sell and deliver Licensed Discovery Sessions if: (a) the session is co-delivered with an individual carrying a “Master Coach” Holacracy certification, or such an individual actively coaches you while you prepare for delivery and plan follow-up actions; and (b) you use a standard session design, session objectives, and the Licensed Materials provided by HolacracyOne, with no significant additions or changes unless approved by the Master Coach working with you on the delivery.\n•\tYou may only sell and deliver Licensed Services if a Certified Holacracy Coach is also actively leading and working on that engagement and supervising your delivery; you may also not facilitate circles brand new to Holacracy practice, until a Certified Holacracy Coach has facilitated and coached them to a basic level of understanding and signed-off that they are ready for your facilitation.\n\nCertified Holacracy Coach\n\nIf your highest level of Holacracy Certification is “Certified Holacracy Coach”:\n•\tYou may only deliver Licensed Events of up to 8 hours; they may include live meeting simulations or similar demonstrations, and you may customize the design or materials for the event.  You may not claim such events are teaching skills or otherwise building or resulting in skills for the use or application of Holacracy.\n•\tYou may only sell and deliver Licensed Services if: (a) you are under the regular guidance and coaching of an individual who carries the “Master Coach” Holacracy certification, and (b) that Master Coach continues to believe the engagement for your Licensed Services has a reasonable chance of providing value to the client without harming the brand image and reputation of the Licensed Marks, and (c) you agree to report requested information and metrics to HolacracyOne in order to provide visibility on your service delivery activities.\n\nCertified Holacracy Master Coach\n\nIf your highest level of Holacracy certification is “Certified Holacracy Master Coach”, then this policy has no effect; you may sell and deliver Licensed Offerings in any way that you are otherwise authorized to do so, without further restriction.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 1386,
              "title": "Constitution Steward Role Assignment",
              "body": "The @Constitution_Steward role may only be filled by an individual with a Certified Holacracy Master Coach credential, and any change made by the Circle's Lead Link or another duly-authorized role in the assignment of such @Constitution_Steward role may only be enacted after ensuring the elected Rep Link of the Circle sees no Objections to such proposed change in assignment.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 5027,
              "title": "Creating Public-Facing Accounts",
              "body": "No role may create new public-facing accounts that are typically messaged (e.g. a Twitter account, e-mail address, etc.), without first notifying @Meta-CR.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 738309,
              "title": "Disclosing Holacracy Practice",
              "body": "No role shall publicly disclose in a recorded medium which organizations are practicing Holacracy, unless already in the public record, or with permission from the role primarily engaging in the relationship with the practicing organization.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 3632,
              "title": "Don't Break Finance Processes",
              "body": "Any additions or changes to systems or processes of any circle that affect the movement of funds or tracking of sales or payments require integration with @Finance before those changes may be enacted.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 1385,
              "title": "Duplication of Data",
              "body": "No Partner may publish a copy or duplication of authoritative information, when others may reasonably rely upon the copy, without integrating a clear warning that the publication is a copy and may be out of date, along with a usable reference to the information's original authoritative source.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 646,
              "title": "Expense Payments",
              "body": "A Partner may pay any allowable and authorized Organization expenses needed in any of their Roles via a personal payment method (e.g. on a personal credit card) and the Organization shall reimburse such Partner for such expenses within a reasonable timeframe, provided that (a) such expenses are submitted in alignment with any established policies or generally-accepted standards practiced by the Organization, and (b) the Partner optimizes such spending for economy at least to the same extent they otherwise would were they incurring such expenses personally without reimbursement, and in all cases at least to a reasonable degree.\r\n \r\nA Partner may personally benefit from any such payments, or from products and services so procured, without penalty or further obligation to the Organization, provided that such benefits are de-minimis in nature on a case-by-case basis, and that the Organization does not incur any additional costs for such Partner optimizing attainment of such benefits (examples of typically-allowable benefit optimization include paying expenses on a personal credit card to gain reward points, or choosing specific airlines and flights for travel to maximize frequent flyer miles, provided that such flights are comparably priced to other reasonably-convenient options).\r\n \r\nFurther, as a condition of ongoing partnership in the Organization, each Partner must be able and willing to use a personal payment method to cover regular general expenses required to serve as a productive Partner of the organization (e.g. travel expenses to Partner retreats), as well as to cover reasonably-small miscellaneous expenses occasionally required of the specific Roles such Partner fills (e.g. special supplies, printing materials, etc.).  No Partner shall be obligated to cover unreasonably large or ongoing subscription-based expenses for their Roles via a personal payment method, although they may choose to do so per the preceding paragraphs of this policy.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": 847
              }
            },
            {
              "id": 1829,
              "title": "File Format for Presentation Slides",
              "body": "All presentation slides created by any role must use whatever standard file format is specified by @Operations",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 5553,
              "title": "Financial Relationships & Transactions",
              "body": "Any role may enact a financial relationship or transaction (when otherwise authorized), provided that all of the following are true:\r\n\r\na)  The relationship's transactions will use a currency that's approved by @Finance.\r\n\r\nb)  The role notifies @Bookkeeper to expect a payment before directing the other party to send a payment to the company (requesting an invoice counts, as does entering an order in any @Finance-approved order tracking system).\r\n\r\nc)  If the relationship involves a need to convert one currency to another (e.g. to apply a credit in one currency to an invoice in another), the conversion must be calculated using the Interbank rate + 3% as posted on http://oanda.com as of the date of the conversion.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 998,
              "title": "H1 Service Delivery Treated as Licensee",
              "body": "@HolacracyOne_Service_Delivery shall have a Cross Link into the @Holacracy_Ecosystem circle, under the same terms and authority grants as Licensees.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 641,
              "title": "IP Storage",
              "body": "All HolacracyOne IP in electronic format shall be stored on a shared repository recognized by @Operations.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 4036,
              "title": "Licensees and IP Infringement Cases",
              "body": "No role may authorize an individual or an organization to enter a licensing relationship with HolacracyOne so long as it has an open case of intellectual property infringement with HolacracyOne.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 1300,
              "title": "Licensing Created Content",
              "body": "Any circle that controls a Domain over content it has created may grant licenses to that content through the latest version of the standard Creative Commons Attribution-NonCommercial-NoDerivs-Unported license agreement.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": 847
              }
            },
            {
              "id": 1389,
              "title": "Licensing Cross-Links",
              "body": "The Cross Link from any Licensee invited to cross link into HolacracyOne shall be into the @Holacracy_Ecosystem circle, and the authority of the Cross Link to impact the Domains of the circle shall further extend to the entire source Circle originating such link and all roles within; all provided, however, that the Licensee agrees to enact any Accountabilities placed on the Cross Link Role as if such Accountabilities were directly such source Circle.  This Cross Link shall be established upon request of the Licensee and acceptance of these additional terms.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 251576,
              "title": "Messaging Standards for the Holacracy Brand",
              "body": "These messaging standards are intended to apply internally to HolacracyOne as well as to any company licensed to use the Holacracy brand (i.e. licensees). In order to preserve the Holacracy trademark, all roles releasing content associated with the Holacracy brand shall follow the messaging standards below:\n\nOn official channels controlled by H1 or licensees (e.g. own website, own blog, own documents), the following messaging standards apply: \n\n(a) All prominent mentions of the brand must include a \"®\" symbol next to it. It can be small, stylized, or otherwise made less eye-catching for aesthetic purposes as long as it is present and noticeable. For the purpose of this policy, \"Prominent Mentions\" include the logo or the main appearance of the brand name in the title of any document usually considered authoritative (website, contracts, stand-alone products, etc). Exception: in editorial content (e.g. blog), it's acceptable not to use the ® symbol in the article title, as long as it's clearly mentioned somewhere else in the article.\n\n(b) All printed or digital documents marketing the brand should include the following statement somewhere in the copy, typically at the bottom of the page or the footer of the webpage: \"Holacracy is a trademark of HolacracyOne, LLC.\"\n\n(c) The name \"Holacracy\" should be used consistently without spelling deviation: use it capitalized, don't use a translation (e.g. Holacratie, Holakratie), don't transform it into an adjective (e.g. holacratic).  \n\n(d) Don't use the brand as a common noun (e.g. \"a holacracy\", \"l'holacratie\"), and to the extent practical use it as a qualifier and not as a noun at all (e.g. 'using the Holacracy system' instead of 'using Holacracy')\n\nOn unofficial channels where the tone is conversational (e.g. forums, guest blog posts, interviews), these messaging standards may be deprioritized in favor of keeping a conversational and context-appropriate tone.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 5694,
              "title": "Offering Changes Require Pricing Integration",
              "body": "Before any role significantly changes the deliverables or cost of delivery for any product or service offering, it must propose the intended change to the @Pricing_Strategy role and to whatever role is accountable for defining prices for that offering, and integrate any Objections raised to the amended offering before rolling out the change.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 2172,
              "title": "Password Requirements",
              "body": "Anyone using passwords to secure company-related accounts with access to company assets or sensitive data must ensure those passwords are strong, not duplicated on any other system, not stored anywhere except a highly protected repository, and may not share the actual password text with anyone else.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": 847
              }
            },
            {
              "id": 5556,
              "title": "Payment Plans",
              "body": "No role may enter into a payment plan agreement with a customer, unless explicitly allowed by a role controlling the pricing model for that service.  If allowed by the pricing model, the role offering the payment plan must also align with the following additional requirements:\r\n\r\na)  Payment plans with more than 3 payments must be setup through our automated payment plan setup page (http://holacracy.org/payment-plan-setup), and thus must conform to the payment plan structure supported by that page.\r\n\r\nb)  Before directing someone to the Payment Plan Setup page for an event registration, there must be a registration in the registration system with a payment type of \"bank transfer\", so we can record payments against it.\r\n\r\nc)  Before directing someone to the Payment Plan Setup page for other purposes, a request must first be made to @Bookkeeper to generate an invoice, so we can record payments against it.\r\n\r\nd)  Using the Payment Plan Setup page must be counted as a credit card payment, for the purposes of any extra fees due as a result (see Payment Instructions PDF for details).\r\n\r\ne)  Payment plans with just 2 or 3 payments may either use the payment plan setup page, or may be handled by requesting invoices for each payment due (e.g. one invoice with 50% due on receipt, and another invoice with 50% due in 45 days).",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 3098,
              "title": "Pricing Changes Require Integration",
              "body": "Before any role publishes or changes pricing for an external company offering, it must propose the change to the @Pricing_Strategy role and to whatever role is accountable for defining prices for that offering, and integrate any Objections raised to the new price or pricing model before rolling out the change.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": 847
              }
            },
            {
              "id": 83,
              "title": "Privacy Policy",
              "body": "HolacracyOne will not sell, lease, or share customer personal information.  When customers submit such information, HolacracyOne staff may add them to the company's mailing list, from which they can unsubscribe at any time using a link at the bottom of each e-mail message.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 5554,
              "title": "Processing Refunds",
              "body": "Any role taking payments may further refund payments received within the past 60 days as-needed, as long as the refund is issued in alignment with any relevant policies, and as long as the role executing the refund immediately notifies @Bookkeeper with details about the refund (including to who, how much, for what product/service, and a one-sentence-or-less explanation).",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 4309,
              "title": "Project Prioritization Using Value/ROI",
              "body": "If a Value of a Project has been specified in GlassFrog by a Lead Link, then the ROI calculated from it shall be considered the official Lead Link prioritization.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 3625,
              "title": "Role Assignment Terms",
              "body": "Each role assignment made within this circle and all sub-circles must have a commission term specified along with the assignment, or, if not explicitly specified, shall automatically carry a commission term through the end of the calendar year in which the assignment was made (or the following calendar year if made within two months of year-end).  Each role assignment shall automatically terminate and become unfilled at the end of the defined term, unless renewed by whatever role has authority to make such assignments.  The initial commission term for all current role assignments as of the adoption of this policy shall be the end of the calendar year in which this policy was adopted.\r\n\r\nNo one may remove a partner from a role in a circle more than one month before the end of a commission term, unless a Core or Tenured Partner of the organization (other than the person initiating the removal) confirms that he/she would also make that change if in the relevant role.\r\n\r\nResigning from a role in a circle before the end of a commission term shall require three months advance notice, unless otherwise agreed between the role-filler and whatever role has the authority to assign to that role.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 7547,
              "title": "Special Treatment of Licensed Providers",
              "body": "Licensed Holacracy Providers who signed up prior to July 2015 have a licensing contract that grants their partners any special pricing extended to our own HolacracyOne partners, such as special training registration rates, free or discounted subscriptions to subscription offerings, etc.  Thus, any partners of such a Licensee are invited to engage our services under our own partner pricing, subject to the same terms and conditions we apply to our own partners, and no Role or Sub-Circle may define any pricing policies that prevent this.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 1499644,
              "title": "Spending Authorization",
              "body": "All Partners of the organization are authorized to spend company funds or dispose of company inventory (e.g. books) using their reasonable judgment, in support of the Organization's purpose, within the following constraints:\n\nFor expenses of $20+:\n• You must post to Slack before or simultaneous with the spending, sharing the amount they are spending and the purpose (very rough/brief is fine).  This must be on a Slack channel that all partners are subscribed to, or have been notified may include spending announcements for the general category/purpose of the expense in question.\n\nFor expenses of $100+, or for any recurring expenses (including any pattern of one-off expenses for the same purpose):\n• You must post to Slack (under the same channel rules as above) in advance of spending, and explicitly state your \"intent to spend\" (including amount and purpose, and with the whole channel tagged).  You must then answer any clarifying questions and read any reactions about the spending (you don't need to respond to reactions).  The spending is then automatically authorized 48 hours after you answer the last clarifying question (or after your original intent is stated, if there are no questions), unless any partner posts a request to escalate the decision to whatever other spending authorization processes exist (e.g. Lead Link authorization or a defined budget).\n\nFor expenses of $500+ (including recurring expenses that would add up to $500+ over three months), in addition to the above:\n• You must get at least one other partner who challenges the decision in Slack, by suggesting reasons not to spend the funds, or to spend them on an alternate approach instead (playing \"devil's advocate\" to help you think through it counts).\n• After the challenge, you must re-state your intent to spend the funds (either as originally stated or with amendments), and then get at least two other partners to attest that they would also make that spending decision were they in the relevant role.  Attesting to this must be done by adding an obvious money-related reaction to the partner's Slack post, and no one may add such a reaction to an intent-to-spend post unless they are making this attestation.\n\nFor any recurring expenses:\n• You must document the recurring expense via a role note in GlassFrog, and add a trigger to your individual organizational system to review the need for the expense after some period you believe is appropriate, and at that point re-assess the expense and seek re-authorization if desired for another period.\n\nIn addition, for any spending under this policy:\n\n• The spending must clearly support the purpose or accountabilities of a role you fill, without any reasonable inference that boundaries have been blurred in making the spending decision, either between different roles or between personal and role interests.  For example, a reasonable inference might exist if funding a project you're really personally inspired to work on, but where the link to the explicit purpose/accountabilities of one of your roles would look more like a forced fit or a \"nice story\" vs. a natural way to express the role (to an objective third party).  However, you may still spend even with a reasonable inference of blurred boundaries, *if* you have called out the potential boundary question in your Slack post, thoughtfully considered it, and genuinely believe it is not a case of blurred boundaries.\n\n• You must submit a bill to @Bookkeeper promptly after authorizing the purchase, or pay the bill personally and submit for reimbursement via an expense report within the expense reimbursement process and rules published by @Finance.\n\n----\n\nThe authorization given in this policy is just one possible way to get spending authorization; other methods with different rules may separately exist, and partners may use other methods instead of the above when otherwise authorized and applicable.",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 272,
              "title": "Strategy Meeting Process",
              "body": "Per the Board-specified Constitution amendment, the following \"Strategy Meeting\" process shall be used by each circle as the only method to define Strategies for that circle, unless both Lead Link and Rep Link agree to add or change a Strategy outside of a Strategy Meeting.  This meeting does not count as a Governance Meeting, unless reasonable notice has been given per the Constitution's requirement.\r\n\r\nStrategy Meeting Process:\r\n\r\n1)\tCheck-in Round \r\n\r\n2)\tOrientation:  Review Purpose, Scope, & Accountabilities of Circle, and any Strategies of Super-Circle\r\n\r\n3)      Retrospective:\r\n    a)  Each participant individually and silently reflects, captures, and posts notes covering:\r\n          i)      What was done as a result of the previous Strategy\r\n          ii)      Key facts & events for the circle; external changes, opportunities, trends, data, etc. \r\n    b)  Participants collectively organize individual notes into related/useful groupings\r\n    c)  Facilitator focuses on each grouping one at a time; participants describe/clarify key notes they've added and share reflections; Facilitator captures any tensions that surface on a separate list.\r\n\r\n4)    Strategy Generation:\r\n    a)    Surface ideas:  \"What might make sense to emphasize operationally to address these Tensions?\".  Participants capture ideas individually, then post and describe each.\r\n    b)      Discuss to converge:  \"What Strategy should guide our decision making? What should we emphasize?\"\r\n    c)      Lead Link proposes one or more Strategies; process proposal via IDM\r\n\r\n5)      Unpack the Strategy:\r\n    a)  Each participant reflects upon & captures Projects, Next-Actions, and/or Tensions they will process from each of their Roles to enact the Strategies\r\n    b)  Each participant shares what (tensions, actions, projects, etc.) they've captured to process in a round, if anything \r\n    c)  A space to is allowed to solicit feedback from others and for others to request further Projects/Next-Actions of their Roles \r\n\r\n6)   Closing Round",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 4305,
              "title": "Tracking Tracking Systems",
              "body": "Before launching a new system or significant changes to an existing system for tracking key information that will be relied upon on an ongoing basis by a business process of the organization, all roles must provide reasonable advance notice to @Tracker_Tracker, including access to the system and any details or related information requested",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            },
            {
              "id": 4307,
              "title": "Visual Branding Standards",
              "body": "Any role releasing products and materials that graphically represent the Holacracy or HolacracyOne brands must align with @Brand_Design_ published guidelines and Graphic Chart",
              "links": {
                "role_id": null,
                "circle_id": 25,
                "domain": null
              }
            }
          ],
          "domain": [
            {
              "id": 847,
              "description": "All Company property & ordinary business affairs"
            },
            {
              "id": 7646,
              "description": "Partner Relationships"
            }
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
      },
      {
        "id": 62364,
        "label": null,
        "completed": true,
        "position": 7,
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
        "id": 62366,
        "label": null,
        "completed": true,
        "position": 9,
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
        "id": 62357,
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
        "id": 62367,
        "label": null,
        "completed": true,
        "position": 10,
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
        "id": 62368,
        "label": null,
        "completed": true,
        "position": 11,
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
        "id": 62363,
        "label": null,
        "completed": true,
        "position": 6,
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
        "id": 62348,
        "label": null,
        "completed": true,
        "position": 1,
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
          62362,
          62364,
          62366,
          62357,
          62367,
          62368,
          62363,
          62348
        ]
      }
    }
  ]
}
```


Updating Tactical Meetings (PATCH)
----------------------------------

