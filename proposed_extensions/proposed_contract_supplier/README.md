# Suppliers in contract object

This extension proposes adding a suppliers array to the contract object. 


Motivation
==========

As discussed in [this issue](https://github.com/open-contracting/implementation-and-extensions/issues/7), and raised in a number of other implementation discussions, the current constraint in which suppliers are only named in the award, provides difficulties for modelling the reality of contracting processes in some parts of the world. 

The original motivation for relating award and contract was that:

* A procurement process contract should never exist without an award;
* A contract should not be made with suppliers who have not been named in the award;

Version 1.0 of the standard enforces this by omitting ```suppliers``` from the ```contract``` object, and relating each contract to an ```award``` object via the ```awardID``` property.

However, in procurement processes where one award names many suppliers, and then separate contracts are made with each supplier, this limits the ability of the standard to model details of amounts awarded to each specific supplier without creating many duplicate award records. 

See also standard development issues [103](https://github.com/open-contracting/standard/issues/103) and [117](https://github.com/open-contracting/standard/issues/117)

**Advantages of adding ```suppliers``` to ```contract```**

* Better fit with the procurement processes of a number of countries;
* Allows easily analysis of which suppliers hold a given contract;


**Disadvantages of adding ```suppliers``` to ```contract```**

* Greater duplication of data (though we already have this for items etc, as we recognise the redundancy is useful)
* Standard no longer enforces the award->contract relationship, and makes it possible that publishers may provide contracts, but no awards (this can be mitigated by validation tools that look out for this)

**Questions**

* Should ```suppliers``` be __required__ in the ```contract``` object if this is adopted as part of Version 1.1
* Should ```suppliers``` be limited to a single value in contract? i.e. not an array. There may be a case for this under some procurement systems, but leaving an array allows consortiums to also be represented.


How it would look
==================

The full contracts array would now look as follows:

```json
"contracts": [
    {
        "id": "string",
        "awardID": "string",
        "status": "pending",
        "period": {
            "startDate": "string",
            "endDate": "string"
        },
        "value": {
            "currency": "string",
            "amount": "number"
        },
        "dateSigned": "string",
        "suppliers": [
            {
                "additionalIdentifiers": [
                    {
                        "scheme": "string",
                        "legalName": "string",
                        "id": "string",
                        "uri": "string"
                    }
                ],
                "contactPoint": {
                    "url": "string",
                    "email": "string",
                    "telephone": "string",
                    "name": "string",
                    "faxNumber": "string"
                },
                "identifier": {
                    "scheme": "string",
                    "legalName": "string",
                    "id": "string",
                    "uri": "string"
                },
                "name": "string",
                "address": {
                    "postalCode": "string",
                    "countryName": "string",
                    "streetAddress": "string",
                    "region": "string",
                    "locality": "string"
                }
            }
        ],
        "documents": [
            {
                "description": "string",
                "language": "string",
                "format": "string",
                "url": "string",
                "title": "string",
                "datePublished": "string",
                "documentType": "string",
                "id": "string",
                "dateModified": "string"
            }
        ],
        "description": "string",
        "title": "string",
        "implementation": {
            "milestones": [
                {
                    "status": "met",
                    "documents": [
                        {
                            "description": "string",
                            "language": "string",
                            "format": "string",
                            "url": "string",
                            "title": "string",
                            "datePublished": "string",
                            "documentType": "string",
                            "id": "string",
                            "dateModified": "string"
                        }
                    ],
                    "description": "string",
                    "title": "string",
                    "id": "string",
                    "dueDate": "string",
                    "dateModified": "string"
                }
            ],
            "documents": [
                {
                    "description": "string",
                    "language": "string",
                    "format": "string",
                    "url": "string",
                    "title": "string",
                    "datePublished": "string",
                    "documentType": "string",
                    "id": "string",
                    "dateModified": "string"
                }
            ],
            "transactions": [
                {
                    "amount": {
                        "currency": "string",
                        "amount": "number"
                    },
                    "receiverOrganization": {
                        "scheme": "string",
                        "legalName": "string",
                        "id": "string",
                        "uri": "string"
                    },
                    "uri": "string",
                    "source": "string",
                    "providerOrganization": {
                        "scheme": "string",
                        "legalName": "string",
                        "id": "string",
                        "uri": "string"
                    },
                    "date": "string",
                    "id": "string"
                }
            ]
        },
        "items": [
            {
                "description": "string",
                "classification": {
                    "description": "string",
                    "scheme": "string",
                    "id": "string",
                    "uri": "string"
                },
                "additionalClassifications": [
                    {
                        "description": "string",
                        "scheme": "string",
                        "id": "string",
                        "uri": "string"
                    }
                ],
                "id": "string",
                "unit": {
                    "name": "string",
                    "value": {
                        "currency": "string",
                        "amount": "number"
                    }
                },
                "quantity": "integer"
            }
        ],
        "amendment": {
            "date": "string",
            "changes": [],
            "rationale": "string"
        }
    }
]
```
