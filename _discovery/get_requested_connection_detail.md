---
title: /organizations/connections/request/<uuid>
name: Get Requested Connection Detail
method: GET
position: 1.15
visibility: public
description: Get details of a connection request
right_code: |
  ~~~ json
  {
    uuid: '555b68e5-e407-4b15-b200-6fade8980596',
    created_date: '2017-03-29T20:11:12+00:00',
    modified_date: '2018-03-29T20:11:12+00:00',
    organization_name: 'Bobs Big Boys',
    primary_contact_name: 'Bob',
    primary_contact_phone: '555.867.5309',
    primary_contact_email: 'bob@bigboys.com',
    organization_account_number: '0987654321',
    additional_information: 'I like yodelling',
    requested_integrations: [
      {
        "type": "items",
        "update_frequency": "30 6,12 * * *",
        "file_locations": "ftp://foo:bar@baz.blerg",
        "file_specs": "Special things you should know are: I like long walks on the beach",
        "rules": ""
      }, {
        "type": "orders",
        "update_frequency": "33 * * * *",
        "file_locations": "ftp://foo:bar@baz.blerg",
        "file_specs": "Special things you should know are: I like to get jiggy with it.",
        "rules": "Only big willy style is allowed"
      }, {
        "type": "other",
        "update_frequency": "* * * * *",
        "file_locations": "ftp://foo:bar@baz.blerg",
        "file_specs": "I like big butts and I cannot lie",
        "rules": "Can't deny"
      }, {
        "type": "other",
        "update_frequency": "13 3 3 9 *",
        "file_locations": "ftp://foo:bar@baz.blerg",
        "file_specs": "Annual Purge",
        "rules": "There are no rules"
      },
    ]
    uploaded_files: [
      {
        name: 'Example Item File',
        uuid: '555b68e5-e407-4b15-b200-6fade8980596',
      },{
        name: 'Example Order File',
        uuid: '8988ff95-e82d-4b28-b55f-057c3208c00e',
      },{
        name: 'Example Allocation File',
        uuid: 'a55897c4-3d86-4804-851a-b89654a1d309',
      }
    ]
  }
  ~~~
  {: title="Response" }
---

### Response Parameters:

For the purposes of ease of description, we describe these endpoints as a retailer requesting a connection to a supplier.

created_date
: (string) Date and time the request to connect was received. Formatted as UTC following ISO 8601.

modified_date
: (string) Date and time the request to connect was last modified. Formatted as UTC following ISO 8601.

organization_name:
: (string) The name of supplier.

primary_contact_name:
: (string) The name of the primary contact for the supplier.

primary_contact_phone:
: (string) The phone number for the primary contact.

primary_contact_email:
: (string) The email address for the primary contact.

organization_account_number:
: (string) The retailer's account number in the supplier's system.

additional_information:
: (string) Links to any sample files or specification documentation you may have.

requested_integrations:
: (array) Array of Integration Objects

uploaded_files:
: (array) Array of File Objects previously uploaded by the [#upload endpoint](#filesupload). Sample files or documentation.

#### Integration Objects
type:
: (string) Type of the integration. Options: `item`, `order`, `allocation`, `tracking`, `other`

update_frequency:
: (string) A cron representation of the update frequency for the integration

file_locations:
: (string) Locations (URLs) where the files for this integration can be retrieved

file_specs:
: (string) Specifications of the files

rules:
: (string) Rules and business logic for the integration

#### File Object
name:
: (string) Name of the file

uuid:
: (string) The Universal Unique Identifier of the uploaded file
