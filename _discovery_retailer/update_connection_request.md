---
title: /organizations/connections/request/&ltuuid&gt/
name: Update Connection Request
position: 3.05
visibility: public
method: patch
description:
right_code: |
  ~~~ json
  {
    "organization_name": "Thomas-Perkins",
    "primary_contact_name": "owner user",
    "primary_contact_phone": "801-555-1212",
    "primary_contact_email": "roger@rabbit.com",
    "retailer_account_number": "ABC123",
    "additional_information": "What's up doc",
    "integrations": [
      {
        "record_uuid": "3a438d7e-1234-46e1-96d2-efd9dac561d9",
        "integration_type": "items",
        "update_frequency": "* 20 12 3 8,9 *",
        "file_specs": "items specs",
        "rules": "if you can't say anything nice, don't say anything at all"
      }
    ]
  }
  ~~~
  {: title="Request" }


---
### URL Parameters:

uuid
: (string) The Universal Unique Identifier for the connection request

### Request Parameters:

For ease of description, we describe these endpoints as a retailer requesting a connection to a supplier.

### Optional:

organization_name:
: (string) The name of supplier.  Note: this is returned as org_name in the other connection responses

primary_contact_name:
: (string) The name of the primary contact for the supplier. Note: this is returned as org_contact_full_name in other connection responses

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

<!-- task-github-127 Create Integration include file -->

#### Integration Objects
type:
: (string) Type of the integration. Options: "item", "order", "allocation", "tracking", "other"

update_frequency:
: (string) A cron representation of the update frequency for the integration

file_locations:
: (string) Locations (URLs) where the files for this integration can be retrieved

file_specs:
: (string) Specifications of the files

rules:
: (string) Rules and business logic for the integration

<!-- task-github-127 Create File include file -->

#### File Object

{% include objects/file_upload.md %}

### Expected Response Codes

Expected reponse code is 204.


{% include links/response_codes.md %}


~~~ bash
curl -X "PATCH" "https://api-sandbox.cruxconnect.com/organizations/connections/request/d0041bf9-ee07-4298-8298-26eee419db2d/" \
     -H 'Cookie: sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp' \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "integrations": [
    {
      "rules": "if you can'"'"'t say anything nice, don'"'"'t say anything at all",
      "file_specs": "items specs",
      "record_uuid": "3a438d7e-1234-46e1-96d2-efd9dac561d9",
      "update_frequency": "* 20 12 3 8,9 *",
      "integration_type": "items"
    }
  ],
  "retailer_account_number": "ABC123",
  "additional_information": "What'"'"'s up doc",
  "primary_contact_name": "owner user",
  "primary_contact_phone": "801-555-1212",
  "organization_name": "Thomas-Perkins",
  "primary_contact_email": "roger@rabbit.com"
}'

~~~
{: title="Curl" }

~~~ bash
http --json PATCH 'https://api-sandbox.cruxconnect.com/organizations/connections/request/d0041bf9-ee07-4298-8298-26eee419db2d/' \
    'Cookie':'sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    integrations:="[
  {
    \"rules\": \"if you can't say anything nice, don't say anything at all\",
    \"file_specs\": \"items specs\",
    \"record_uuid\": \"3a438d7e-1234-46e1-96d2-efd9dac561d9\",
    \"update_frequency\": \"* 20 12 3 8,9 *\",
    \"integration_type\": \"items\"
  }
]" \
    retailer_account_number="ABC123" \
    additional_information="What's up doc" \
    primary_contact_name="owner user" \
    primary_contact_phone="801-555-1212" \
    organization_name="Thomas-Perkins" \
    primary_contact_email="roger@rabbit.com"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Update Connection Request
    # PATCH https://api-sandbox.cruxconnect.com/organizations/connections/request/d0041bf9-ee07-4298-8298-26eee419db2d/

    try:
        response = requests.patch(
            url="https://api-sandbox.cruxconnect.com/organizations/connections/request/d0041bf9-ee07-4298-8298-26eee419db2d/",
            headers={
                "Cookie": "sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp",
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    integrations:="[
  {
    \"rules\": \"if you can't say anything nice, don't say anything at all\",
    \"file_specs\": \"items specs\",
    \"record_uuid\": \"3a438d7e-1234-46e1-96d2-efd9dac561d9\",
    \"update_frequency\": \"* 20 12 3 8,9 *\",
    \"integration_type\": \"items\"
  }
]" \
    retailer_account_number="ABC123" \
    additional_information="What's up doc" \
    primary_contact_name="owner user" \
    primary_contact_phone="801-555-1212" \
    organization_name="Thomas-Perkins" \
    primary_contact_email="roger@rabbit.com")
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
// request Update Connection Request
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/organizations/connections/request/d0041bf9-ee07-4298-8298-26eee419db2d/',
        method: 'PATCH',
        headers: {"Cookie":"sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp","Authorization":"Token 1234567890","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"organization_name\":\"Thomas-Perkins\",\"primary_contact_name\":\"owner user\",\"primary_contact_phone\":\"801-555-1212\",\"primary_contact_email\":\"roger@rabbit.com\",\"retailer_account_number\":\"ABC123\",\"additional_information\":\"What's up doc\",\"integrations\":[{\"record_uuid\":\"3a438d7e-1234-46e1-96d2-efd9dac561d9\",\"integration_type\":\"items\",\"update_frequency\":\"* 20 12 3 8,9 *\",\"file_specs\":\"items specs\",\"rules\":\"if you can't say anything nice, don't say anything at all\"}]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
