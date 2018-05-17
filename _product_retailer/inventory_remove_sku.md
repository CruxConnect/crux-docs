---
title: /products/inventory-lists/&lt;inventory_list_uuid&gt;/remove-skus/
name: Inventory Remove SKU
position: 11.08
visibility: public
method: post
description: Remove SKUs from an existing Inventory List for your account
right_code: |
  ~~~ json
  {
    "sku_uuids": [
      "26476fbe-3427-4648-9925-2090e06a41e9"
    ]
  }
  ~~~
  {: title="Request" }


---
Remove SKUs from an existing Inventory List for your account.

### URL Parameters

inventory_list_uuid
: (string) Universal Unique Identifier for the Inventory List

### Request Parameters:

skus
: (array) The SKUs parameter holds sku_uuids for all of the SKUs you wish to add to your Inventory List

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/remove-skus/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "sku_uuids": [
    "26476fbe-3427-4648-9925-2090e06a41e9"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/remove-skus/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    sku_uuids:="[
  \"26476fbe-3427-4648-9925-2090e06a41e9\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Inventory Remove SKU
    # POST https://api-sandbox.cruxconnect.com/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/remove-skus/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/remove-skus/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    sku_uuids:="[
  \"26476fbe-3427-4648-9925-2090e06a41e9\"
]")
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
// request Inventory Remove SKU
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/remove-skus/',
        method: 'POST',
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
    request.write("{\"sku_uuids\":[\"26476fbe-3427-4648-9925-2090e06a41e9\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
