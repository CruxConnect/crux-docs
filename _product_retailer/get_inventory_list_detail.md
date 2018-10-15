---
title: /timp/products/inventory-lists/&lt;inventory_list_uuid&gt;/
name: Get Inventory List Detail
position: 4.01
visibility: public
method: get
description: Get the Details of a particular Inventory List you have access to
right_code: |
  ~~~ json
  {
    "uuid": "fef4116d-7a13-4dcf-a40c-10faa19f562c",
    "retailer": {
      "uuid": "7b438288-bc88-4247-ac12-84e4519854fb"
    },
    "skus": [
      {
        "uuid": "26476fbe-3427-4648-9925-2090e06a41e9"
      },
    ],
    "created": "2018-04-24T23:48:19.876044Z",
    "last_updated": "2018-04-24T23:48:19.876086Z",
    "name": "The enormous grass inventory list",
    "description": "When it's all said and done, there's still enormous grass inventory list."
  }
  ~~~
  {: title="Response" }

---
Get the Details of a particular Inventory List you have access to.

### URL Parameters

inventory_list_uuid
: (string) Universal Unique Identifier for the Inventory List

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Inventory List

retailer
: (object) The Retailer object contains a single retailer_uuid.

skus
: (array) The SKUs list parameter contains a list of SKU objects containing a single sku_uuid each

created
: (string) The Created parameter is the date the Catalog was Created.

last_updated
: (string) The Last Updated parameter is the date the Catalog was Last Updated.

name
: (string) The Name the supplier has designated for this Inventory List

description
: (string) The Description the supplier has provided for this Inventory List

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/timp/products/inventory-lists/fef4116d-7a13-4dcf-a40c-10faa19f562c/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/timp/products/inventory-lists/fef4116d-7a13-4dcf-a40c-10faa19f562c/' \
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
    # Get Inventory List Detail
    # GET https://api-sandbox.cruxconnect.com/timp/products/inventory-lists/fef4116d-7a13-4dcf-a40c-10faa19f562c/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/timp/products/inventory-lists/fef4116d-7a13-4dcf-a40c-10faa19f562c/",
            headers={
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
// request Get Inventory List Detail
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/products/inventory-lists/fef4116d-7a13-4dcf-a40c-10faa19f562c/',
        method: 'GET',
        headers: {"Authorization":"Token 1234567890","Content-Type":"application/json; charset=utf-8"}
    };
    httpOptions.headers['User-Agent'] = 'node ' + process.version;


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
