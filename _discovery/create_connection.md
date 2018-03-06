///// Should this file be in Organizations?
---
title: /discovery/create
///// maybe: /connections/create
name: Create Connection
method: POST
description: Initiate a formal connection in Crux between a retailer and a supplier
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
: (string) Phone number of the Person

Optional: none


### Response Parameters:

///// Should return a full connection object (like in get_connections.md) or just a connection UUID and a request_date?
///// Should we just return a generic 'success' message and send a confirmation email the same time we send an email to the account manager?

uuid
: (string) Universal Unique Identifier for the connection

request_date
: (string) date the connection was requested
