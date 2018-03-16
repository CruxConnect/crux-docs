---
title: /account/request-connection <!--TODO: not the final location-->
name: Request a Connection
method: POST
position: 1.15
visibility: public
description: Initiate a connection request between a retailer and a supplier
---

### Request Parameters:

For the purposes of ease of description, we describe these endpoints as a retailer requesting a connection to a supplier.

Required:

organization_name:
: (string) The name of supplier.

primary_contact_name:
: (string) The name of the primary contact for the supplier.

Optional:

primary_contact_phone:
: (string) The phone number for the primary contact.

primary_contact_email:
: (string) The email address for the primary contact.

integration_account_number:
: (string) The retailer's account number in the supplier's system.

integration_file_locations:
: (string) Locations where the files needed for integration can be found.

integration_file_specifications:
: (string) Specifications regarding the files needed for integration.

integration_file_update_frequencies:
: (string) Notes regarding the frequency of file updates.

integration_rules:
: (string) Notes regarding business logic for the integration.

additional_information:
: (string) Links to any sample files or specification documentation you may have.

uploaded_files:
: (array) Array of File Objects previously uploaded by the [#upload endpoint](#filesupload). Sample files or documentation.

#### File Object
name:
: (string) Name of the file

uuid:
: (string) The Universal Unique Identifier of the uploaded file

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the connection

request_date
: (string) Date and time the request to connect was received. Formatted as UTC following ISO 8601.
