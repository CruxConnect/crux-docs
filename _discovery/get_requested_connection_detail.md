---
title: /organizations/connections/request/&ltuuid&gt/
name: Get Requested Connection Detail
position: 3.04
visibility: public
method: get
description: Get details of a specific connection request
right_code: |
  ~~~ json
  {
    "integrations": [
      {
        "record_uuid": "43e75dbc-20cd-488a-b904-8c1910904ec5",
        "integration_type": "items",
        "update_frequency": null,
        "feed_source_file_locations": "items locs",
        "file_specs": "items specs",
        "rules": "items rules",
        "date_created": "2018-04-09"
      },
      {
        "record_uuid": "08fffe73-c1c5-47a9-b18e-13d7259c1e9b",
        "integration_type": "orders",
        "update_frequency": "* 30 12 * * 2",
        "feed_source_file_locations": "orders locs",
        "file_specs": "orders specs",
        "rules": "orders rules",
        "date_created": "2018-04-09"
      }
    ],
    "uploaded_files": [
      {
        "name": "Example Item File",
        "uuid": "555b68e5-e407-4b15-b200-6fade8980596",
      }
    ],
    "record_uuid": "6c822de1-8f9a-48ca-87c1-c5c788a6caf3",
    "org_name": "G",
    "org_contact_full_name": "g",
    "primary_contact_phone": "g",
    "primary_contact_email": "g@g.gg",
    "retailer_account_number": "",
    "additional_information": "",
    "request_date": "2018-04-09",
    "is_approved": true,
    "approved_by": {
      "uuid": "6cf0bb8b-442e-43c4-8bbe-bc823e17981e",
      "person": {
        "uuid": "cfcc3db3-dbfd-4019-be0a-2858e08a760a",
        "first_name": "Joe",
        "last_name": "Account",
        "email": "joe@cruxaccountmanager.com",
        "phone": "717.334.5425x58894",
        "job_title": "Account Manager"
      }
  }
  ~~~
  {: title="Response" }

---
Get details of a specific connection request

### URL Parameters:

record_uuid
: (string) The Universal Unique Identifier for the Requested Connection

### Response Parameters:

For the purposes of ease of description, we describe these endpoints as a retailer requesting a connection to a supplier.

<!-- task-github-127 Create Connection Request include file -->

integrations
: (object) Integrations to including `item`, `order`, `allocation`, `tracking`, `other`

uploaded_files:
: (array) Array of File Objects previously uploaded by the [#upload endpoint](#filesupload). Sample files or documentation.

org_contact_full_name
: (string) Full name of the organization contact

primary_contact_phone
: (string) Phone number for the orgainzation primary contact

primary_contact_email
: (string) Email address for the orgainzation primary contact

retailer_account_number or supplier_account_number:
: (string) The retailer's account number in the supplier's system.

additional_information:
: (string) Links to any sample files or specification documentation you may have.

request_date
: (string) Date and time the request to connect was received. Formatted as UTC following ISO 8601.

is_approved
: (boolean) Approval status of the connection request

approved_by
: (object) Who approved the participation including a uuid and details on the person


<!-- task-github-127 Create Integration include file -->

#### Integration Objects

record_uuid
: (object) UUID for the integration

integration_type
: (string) Type of the integration. Options: "item", "order", "allocation", "tracking", "other"

update_frequency
: (string) A cron representation of the update frequency for the integration

feed_source_file_locations
: (string) Locations (URLs) where the files for this integration can be retrieved

file_specs
: (string) Specifications of the files

rules
: (string) Rules and business logic for the integration

date_created
: (string) Date the integration was created

#### Approved By
uuid
: (string) The Universal Unique Identifier for the Approval Object

person
: (object) Person who approved the discovery participation request

#### Person

{% include objects/contact.md %}

<!-- task-github-127 Create File include file -->
#### File Object

name:
: (string) Name of the file

uuid:
: (string) The Universal Unique Identifier of the uploaded file

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl "https://api-dev.cruxconnect.com/organizations/connections/request/6c822de1-8f9a-48ca-87c1-c5c788a6caf3/" \
     -H 'Cookie: sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp' \
     -H 'Authorization: Token 1234567890'

~~~
{: title="Curl" }

~~~ bash
http GET 'https://api-dev.cruxconnect.com/organizations/connections/request/6c822de1-8f9a-48ca-87c1-c5c788a6caf3/' \
    'Cookie':'sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp' \
    'Authorization':'Token 1234567890'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Get Requested Connection Detail
    # GET https://api-dev.cruxconnect.com/organizations/connections/request/6c822de1-8f9a-48ca-87c1-c5c788a6caf3/

    try:
        response = requests.get(
            url="https://api-dev.cruxconnect.com/organizations/connections/request/6c822de1-8f9a-48ca-87c1-c5c788a6caf3/",
            headers={
                "Cookie": "sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp",
                "Authorization": "Token 1234567890",
            },
        )
        print('Response HTTP Status Code: {status_code}'.format(
            status_code=response.status_code))
        print('Response HTTP Response Body: {content}'.format(
            content=response.content))
    except requests.exceptions.RequestException:
        print('HTTP Request failed')

~~~
{: title="Python (requests)" }

~~~ javascript
// request Get Requested Connection Detail
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/organizations/connections/request/6c822de1-8f9a-48ca-87c1-c5c788a6caf3/',
        method: 'GET',
        headers: {"Cookie":"sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp","Authorization":"Token 1234567890"}
    };
    httpOptions.headers['User-Agent'] = 'node ' + process.version;

    // Paw Store Cookies option is not supported

    const request = httpTransport.request(httpOptions, (res) => {
        let responseBufs = [];
        let responseStr = '';

        res.on('data', (chunk) => {
            if (Buffer.isBuffer(chunk)) {
                responseBufs.push(chunk);
            }
            else {
                responseStr = responseStr + chunk;
            }
        }).on('end', () => {
            responseStr = responseBufs.length > 0 ?
                Buffer.concat(responseBufs).toString(responseEncoding) : responseStr;

            callback(null, res.statusCode, res.headers, responseStr);
        });

    })
    .setTimeout(0)
    .on('error', (error) => {
        callback(error);
    });
    request.write("")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
