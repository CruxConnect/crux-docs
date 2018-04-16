---
title: /discovery/participation/&ltuuid&gt/
name: Get Discovery Participation
position: 8.00
visibility: internal
method: get
description: Get Discovery Catalog Participation
right_code: |
  ~~~ json
  {
    "supplier_uuid": "963e4549-712b-42d7-8bd9-34eb21d15ea9",
    "is_participating": true,
    "discovery_catalog_uuid": "ecb49a47-714f-4d37-927d-21921738d681",
    "date_joined": "2018-04-06",
    "requested_by": {
      "uuid": "507368a9-b52c-47c2-8f18-681ed95ff27f",
      "first_name": "",
      "last_name": "",
      "email": "kweaver@projectzuul.com",
      "phone": "483-900-7133",
      "job_title": "Account Manager"
    },
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
  }
  ~~~
  {: title="Response" }

---
Get Supplier participation in the Discovery Catalog and, if participating, the catalog the Supplier will use as their Discovery Catalog

### URL Parameters
supplier_uuid
: (uuid) The Universal Unique Identifier for the Supplier

### Response

supplier_uuid
: (string) The Universal Unique Identifier for the Supplier

is_participating
: (bool) Whether or not the Supplier is participating in Discovery Catalog

discovery_catalog_uuid
: (string) The Universal Unique Identifier for the Discovery Catalog. Required if participation is true.  Empty/Ignored if not participating.

date_joined
: (string) Most recent date supplier made themselves visible in the discovery catalog

requested_by
: (object) Person Object for supplier employee who requested the supplier's visibility in the Discovery Marketplace.

approved_by
: (object) Crux employee who approved the supplier's visibility in the Discovery Marketplace

#### Requested By
<!-- task-github-127 use Person include file -->

{% include objects/contact.md %}

#### Approved By

uuid
: (string) The Universal Unique Identifier

person
: (object) Person who approved the discovery participation request

#### Person

{% include objects/contact.md %}

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl "https://api-dev.cruxconnect.com/discovery/participation/963e4549-712b-42d7-8bd9-34eb21d15ea9/" \
     -H 'Cookie: sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp' \
     -H 'Authorization: Token 01234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-dev.cruxconnect.com/discovery/participation/963e4549-712b-42d7-8bd9-34eb21d15ea9/' \
    'Cookie':'sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp' \
    'Authorization':'Token 01234567890' \
    'Content-Type':'application/json; charset=utf-8'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Discovery Participation
    # GET https://api-dev.cruxconnect.com/discovery/participation/963e4549-712b-42d7-8bd9-34eb21d15ea9/

    try:
        response = requests.get(
            url="https://api-dev.cruxconnect.com/discovery/participation/963e4549-712b-42d7-8bd9-34eb21d15ea9/",
            headers={
                "Cookie": "sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp",
                "Authorization": "Token 01234567890",
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
// request Get Discovery Participation
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/discovery/participation/963e4549-712b-42d7-8bd9-34eb21d15ea9/',
        method: 'GET',
        headers: {"Cookie":"sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp","Authorization":"Token 01234567890","Content-Type":"application/json; charset=utf-8"}
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
