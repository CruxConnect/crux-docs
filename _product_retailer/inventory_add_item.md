---
title: /products/inventory-lists/&lt;inventory_list_uuid&gt;/add-items/
name: Inventory Add Item
position: 11.03
visibility: public
method: post
description: Add Items to an existing Inventory List for your account
right_code: |
  ~~~ json
  {
    "item_uuids": [
      "6dc3646a-8719-483e-8b4c-617215fb1bf0"
    ]
  }
  ~~~
  {: title="Request" }


---
Add Items to an existing Inventory List for your account.

To create an inventory list see [Create Inventory List](/#product_retailercreate_inventory_list)

To add SKUs to an Inventory List see [Inventory Add Item](/#product_retailerinventory_add_sku).

### URL Parameters

inventory_list_uuid
: (string) Universal Unique Identifier for the Inventory List

### Request Parameters:

item_uuids
: (array) An array of item_uuids for all of the items you wish to add to your Inventory List

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/add-items/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "item_uuids": [
    "6dc3646a-8719-483e-8b4c-617215fb1bf0"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/add-items/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    item_uuids:="[
  \"6dc3646a-8719-483e-8b4c-617215fb1bf0\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Inventory Add Item
    # POST https://api-sandbox.cruxconnect.com/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/add-items/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/add-items/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    item_uuids:="[
  \"6dc3646a-8719-483e-8b4c-617215fb1bf0\"
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
// request Inventory Add Item
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/add-items/',
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
    request.write("{\"item_uuids\":[\"6dc3646a-8719-483e-8b4c-617215fb1bf0\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
