---
title: Discovery
name:
position: 9
visibility: file-specs
method:
description: Discovering stuff
right_code: |

---

#### Discovery
_Retailer Fields_

organization_name
: (string) ***Required*** The name of supplier.

primary_contact_name
: (string) ***Required*** The name of the primary contact for the supplier.

primary_contact_phone
: (string) The phone number for the primary contact.

primary_contact_email
: (string) The email address for the primary contact.

organization_account_number
: (string) The retailer’s account number in the supplier’s system.

additional_information
: (string) Links to any sample files or specification documentation you may have.

requested_integrations
: (object) Array of Integration Object

uploaded_files
: (object) Array of File Objects previously uploaded by the #upload endpoint. Sample files or documentation.

#### request_integration (object)
_Retailer Fields_

type
: (string/enum) Type of the integration. Accepted Values below.
- “item”
- “order”
- “allocation”
- “tracking”
- “other”

update_frequency
: (string) A cron representation of the update frequency for the integration

file_locations
: (string) Locations (URLs) where the files for this integration can be retrieved

file_specs
: (string) Specifications of the files

rules
: (string) Rules and business logic for the integration

#### file (object)

name
: (string) Name of the file

uuid
: (string) The Universal Unique Identifier of the uploaded file. (For clarity: the UUID goes with the upload, not the file. If you upload the exact same file more than once, each upload will have its own UUID.)


