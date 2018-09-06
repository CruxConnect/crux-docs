---
title: /timp/organizations/connections/request/
name: Request Connection
position: 1.00
visibility: public
method: post
description: Initiate a connection request between a retailer and a supplier
right_code: |
  ~~~ json
  {
    "organization_name": "Bob Big Boy",
    "primary_contact_name": "Bob Brown",
    "primary_contact_phone": "801-555-1212",
    "primary_contact_email": "bob@bigboy.io",
    "additional_information": "Oh, It's you Bob",
    "integrations": [
      {
        "type": "items",
        "update_frequency": "30 6,12 * * *",
        "file_locations": "ftp://foo:bar@baz.blerg",
        "rules": "No winers"
      },
      {
        "type": "order",
        "update_frequency": "33 * * * *",
        "file_locations": "file_locations",
        "file_specs": "Special things you should know are: I like to get jiggy with it.",
        "rules": "Only big willy style is allowed"
      },
      {
        "type": "other",
        "update_frequency": "ftp://foo:bar@baz.blerg",
        "file_specs": "Special things you should know are: I like long walks on the beach",
        "rules": "No Rules, Just Fun"
      }
    ],
    "uploaded_files": []
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "request_uuid": "d0d0b571-4839-47e2-9f30-4db9df584529",
    "request_date": "2018-08-21 23:38:33.070681+00:00"
  }
  ~~~
  {: title="Response" }

---
Initiate a connection request between a retailer and a supplier

### Request Parameters:

For ease of description, we describe these endpoints as a retailer requesting a connection to a supplier.

organization_name:
: (string) The name of supplier.

primary_contact_name:
: (string) The name of the primary contact for the supplier.

### Optional

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

{% include timp/objects/file_upload.md %}

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the connection

request_date
: (string) Date and time the request to connect was received. Formatted as UTC following ISO 8601.

### Response Code:

{% include timp/links/response_codes.md %}

### Expected Response Codes

# Short Description

Initiate a connection request between a retailer and a supplier

# Long Description

Initiate a connection request between a retailer and a supplier

### Request Parameters:

For ease of description, we describe these endpoints as a retailer requesting a connection to a supplier.

organization_name:
: (string) The name of supplier.

primary_contact_name:
: (string) The name of the primary contact for the supplier.

### Optional

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

{% include timp/objects/file_upload.md %}

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the connection

request_date
: (string) Date and time the request to connect was received. Formatted as UTC following ISO 8601.

### Response Code:

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/timp/organizations/connections/request/" \
     -H 'Authorization: Token `1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -H 'Cookie: sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz' \
     -d $'{
  "integrations": [
    {
      "rules": "No winers",
      "file_locations": "ftp://foo:bar@baz.blerg",
      "type": "items",
      "update_frequency": "30 6,12 * * *"
    },
    {
      "rules": "Only big willy style is allowed",
      "file_locations": "file_locations",
      "file_specs": "Special things you should know are: I like to get jiggy with it.",
      "type": "order",
      "update_frequency": "33 * * * *"
    },
    {
      "rules": "No Rules, Just Fun",
      "file_specs": "Special things you should know are: I like long walks on the beach",
      "type": "other",
      "update_frequency": "ftp://foo:bar@baz.blerg"
    }
  ],
  "uploaded_files": [],
  "additional_information": "Oh, It'"'"'s you Bob",
  "primary_contact_name": "Bob Brown",
  "primary_contact_phone": "801-555-1212",
  "organization_name": "Bob Big Boy",
  "primary_contact_email": "bob@bigboy.io"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/timp/organizations/connections/request/' \
    'Authorization':'Token `1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    'Cookie':'sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz' \
    integrations:="[
  {
    \"rules\": \"No winers\",
    \"file_locations\": \"ftp://foo:bar@baz.blerg\",
    \"type\": \"items\",
    \"update_frequency\": \"30 6,12 * * *\"
  },
  {
    \"rules\": \"Only big willy style is allowed\",
    \"file_locations\": \"file_locations\",
    \"file_specs\": \"Special things you should know are: I like to get jiggy with it.\",
    \"type\": \"order\",
    \"update_frequency\": \"33 * * * *\"
  },
  {
    \"rules\": \"No Rules, Just Fun\",
    \"file_specs\": \"Special things you should know are: I like long walks on the beach\",
    \"type\": \"other\",
    \"update_frequency\": \"ftp://foo:bar@baz.blerg\"
  }
]" \
    uploaded_files:="[]" \
    additional_information="Oh, It's you Bob" \
    primary_contact_name="Bob Brown" \
    primary_contact_phone="801-555-1212" \
    organization_name="Bob Big Boy" \
    primary_contact_email="bob@bigboy.io"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Request Connection
    # POST https://api-sandbox.cruxconnect.com/timp/organizations/connections/request/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/timp/organizations/connections/request/",
            headers={
                "Authorization": "Token `1234567890",
                "Content-Type": "application/json; charset=utf-8",
                "Cookie": "sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz",
            },
            data=json.dumps(    integrations:="[
  {
    \"rules\": \"No winers\",
    \"file_locations\": \"ftp://foo:bar@baz.blerg\",
    \"type\": \"items\",
    \"update_frequency\": \"30 6,12 * * *\"
  },
  {
    \"rules\": \"Only big willy style is allowed\",
    \"file_locations\": \"file_locations\",
    \"file_specs\": \"Special things you should know are: I like to get jiggy with it.\",
    \"type\": \"order\",
    \"update_frequency\": \"33 * * * *\"
  },
  {
    \"rules\": \"No Rules, Just Fun\",
    \"file_specs\": \"Special things you should know are: I like long walks on the beach\",
    \"type\": \"other\",
    \"update_frequency\": \"ftp://foo:bar@baz.blerg\"
  }
]" \
    uploaded_files:="[]" \
    additional_information="Oh, It's you Bob" \
    primary_contact_name="Bob Brown" \
    primary_contact_phone="801-555-1212" \
    organization_name="Bob Big Boy" \
    primary_contact_email="bob@bigboy.io")
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
// request Request Connection
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/organizations/connections/request/',
        method: 'POST',
        headers: {"Authorization":"Token `1234567890","Content-Type":"application/json; charset=utf-8","Cookie":"sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz"}
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
    request.write("{\"organization_name\":\"Bob Big Boy\",\"primary_contact_name\":\"Bob Brown\",\"primary_contact_phone\":\"801-555-1212\",\"primary_contact_email\":\"bob@bigboy.io\",\"additional_information\":\"Oh, It's you Bob\",\"integrations\":[{\"type\":\"items\",\"update_frequency\":\"30 6,12 * * *\",\"file_locations\":\"ftp://foo:bar@baz.blerg\",\"rules\":\"No winers\"},{\"type\":\"order\",\"update_frequency\":\"33 * * * *\",\"file_locations\":\"file_locations\",\"file_specs\":\"Special things you should know are: I like to get jiggy with it.\",\"rules\":\"Only big willy style is allowed\"},{\"type\":\"other\",\"update_frequency\":\"ftp://foo:bar@baz.blerg\",\"file_specs\":\"Special things you should know are: I like long walks on the beach\",\"rules\":\"No Rules, Just Fun\"}],\"uploaded_files\":[]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
