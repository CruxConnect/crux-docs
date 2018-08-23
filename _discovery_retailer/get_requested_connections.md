---
title: /timp/organizations/connections/request/
name: Get Requested Connections
position: 1.01
visibility: public
method: get
description: Get a list of requested connections
right_code: |
  ~~~ json
  {
    "requests": [],
    "pagination": {
      "total_count": 0,
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

<!-- task-github-127 Create Connection Request include file -->
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
: (object) Crux employee who approved the supplier's visibility in the Discovery Marketplace.


{% include timp/objects/response_pagination.md %}

#### Integration Objects

record_uuid
: (object) UUID for the integration

integration_type
: (string) Type of the integration. Options: `item`, `order`, `allocation`, `tracking`, `other`

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
: (string) The Universal Unique Identifier
person
: (object) Person Object for the Crux employee who approved the supplier's visibility in the Discovery Marketplace.

#### Person

{% include timp/objects/contact.md %}

#### File Object

{% include objects/file_upload.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-dev.cruxconnect.com/timp/organizations/connections/request/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -H 'Cookie: sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-dev.cruxconnect.com/timp/organizations/connections/request/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    'Cookie':'sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Requested Connections
    # GET https://api-dev.cruxconnect.com/timp/organizations/connections/request/

    try:
        response = requests.get(
            url="https://api-dev.cruxconnect.com/timp/organizations/connections/request/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
                "Cookie": "sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz",
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
// request Get Requested Connections
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/timp/organizations/connections/request/',
        method: 'GET',
        headers: {"Authorization":"Token 1234567890","Content-Type":"application/json; charset=utf-8","Cookie":"sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz"}
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
