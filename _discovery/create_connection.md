---
title: /discovery/create
///// maybe: /connections/create
name: Create Connection
method: POST
description: Initiate a formal connection in Crux between a retailer and a supplier
right_code: |
  ~~~ json
  {
    "supplier_uuid": "9b3314d7-a280-4ed4-bf5c-83e3c9b013c0",
    "supplier_name": "Really Cool Supplier",
    "retailer_uuid": "2e0ecb7e-9426-4e66-a8a9-e69cd8c806c0",
    "requested_by": {
      "uuid": "45d9c4a6-0bf0-4fa6-95df-c421ddba16e5",
      "first_name": "Asher",
      "last_name": "Lev",
      "email": "alev@veryawesomeretailer.com",
      "phone": "1 (409) 963-7765",
    }
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "connection_uuid": "97fa8fdf-6b94-409e-a684-841d42605881",
    "request_date": "2017-10-30T22:21:40.123456Z"
  }
  ~~~
  {: title="Response" }

---
### Request Parameters:

Required:
supplier_uuid
: (string) Supplier's organization UUID.

supplier_name
: (string) Supplier's standardized name.

retailer_uuid
: (string) Retailer's organization UUID.

requested_by
: (object) Person object for individual initiating the request.

#### Person Object:

uuid
: UUID for the Person

first_name
: (string) First Name of the Person

last_name
: (string) Last Name of the Person

email
: (string) Email address of the Person

phone
: (string) Phone number of the Person. Format is not specified but must contain no more than 20 characters.

Optional: none


### Response Parameters:

uuid
: (string) Universal Unique Identifier for the connection

request_date
: (string) Date and time the request to connect was received. Formatted as UTC following ISO 8601.
