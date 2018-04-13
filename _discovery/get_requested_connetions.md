---
title: /organizations/connections/request/
name: Get Requested Connections Detail
position: 3.03
visibility: public
method: get
description: Get a list of requested connections
right_code: |
  ~~~ json
  {}
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "requests": [
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
        "is_approved": false,
        "approved_by": null
      },
      {
        "integrations": [
          {
            "record_uuid": "3a438d7e-1234-46e1-96d2-efd9dac561d9",
            "integration_type": "items",
            "update_frequency": "* 20 12 3 8,9 *",
            "feed_source_file_locations": null,
            "file_specs": null,
            "rules": null,
            "date_created": "2018-04-10"
          }
        ],
        "uploaded_files": [],
        "record_uuid": "d0041bf9-ee07-4298-8298-26eee419db2d",
        "org_name": "Thomas-Perkins",
        "org_contact_full_name": "owner user",
        "primary_contact_phone": "1-541-219-3109x433",
        "primary_contact_email": "owneruser1@romero.com",
        "retailer_account_number": null,
        "additional_information": null,
        "request_date": "2018-04-10",
        "is_approved": false,
        "approved_by": null
      }
    ],
    "pagination": {
      "total_count": 9,
      "start": 0,
      "limit": 50
    }
  }
  ~~~
  {: title="Response" }

---
Get a list of requested connections


### Request Parameters:

limit
: (int) Number of suppliers displayed on a page; used for paginating results. Default: 50. Maximum: 100. Any 'limit' greater than the Maximum will be forced to the Maximum.

start
: (int) Element number of the first supplier that will be displayed on a page. (The available suppliers are returned in an ordered list, numbered from 0 to Number-of-suppliers, with each supplier an element in the list.) Used for paginating results. Default: 0. If greater than or equal to the number of available suppliers, 'start' is forced to the Number-of-suppliers (which will yield zero results).

### Response Parameters:

requests
: (array) A list of connection request objects (see  Connection Request below)

pagination
: (object) The Pagination object parameter includes the total_count, start, and limit for your Search.


#### Connection Request Object:

integrations
: (object) Integrations to the including `item`, `order`, `allocation`, `tracking`, `other`

uploaded_files
: (object) Uploaded files including the file name the file's UUID.

record_uuid
: (string) UUID of the connection request

org_name
: (string) Name of the organization to which the request is to connect

org_contact_full_name
: (string) Full name of the organization contact

primary_contact_phone
: (string) Phone number for the orgainzation primary contact

primary_contact_email
: (string) Email address for the orgainzation primary contact

retailer_account_number
: (string) Account number for the retailer

additional_information
: (string) Additional information

request_date
: (string) Request date formatted as UTC following ISO 8601.

is_approved
: (boolean) Approval status of the connection request

approved_by
: (string) Name of person approving the request


{% include objects/response_pagination.md %}

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

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl "https://api-dev.cruxconnect.com/organizations/connections/request/" \
     -H 'Cookie: sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp' \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-dev.cruxconnect.com/organizations/connections/request/' \
    'Cookie':'sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Requested Connections Detail
    # GET https://api-dev.cruxconnect.com/organizations/connections/request/

    try:
        response = requests.get(
            url="https://api-dev.cruxconnect.com/organizations/connections/request/",
            headers={
                "Cookie": "sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp",
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps()
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
// request Get Requested Connections Detail
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/organizations/connections/request/',
        method: 'GET',
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
    request.write("{}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
