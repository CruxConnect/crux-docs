---
title: /products/inventory-lists/
name: Create Inventory List
position: 11.02
visibility: public
method: post
description: Create an Inventory List for your account
right_code: |
  ~~~ json
  {
    "name": "New Test Inventory List Name FXu6XvYOGskXhn1v5SAL17IW7AeTImhA",
    "description": "The Description for the New Test Inventory List Name"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "054c051c-891d-4063-a299-62d6e5036e53",
    "retailer": {
      "uuid": "7b438288-bc88-4247-ac12-84e4519854fb"
    },
    "skus": [],
    "created": "2018-05-08T13:37:09.677282Z",
    "last_updated": "2018-05-08T13:37:09.677329Z",
    "name": "New Test Inventory List Name 2BWllm6i28nj7mOpH4K0XqC0UwG4UNRH",
    "description": "The Description for the New Test Inventory List Name"
  }
  ~~~
  {: title="Response" }

---
Create an Inventory Lists for your account.

To add SKUs to an Inventory List see [Inventory Add Item](/#product_retailerinventory_add_sku).

To add items to an Inventory List see [Inventory Add SKU](/#product_retailerinventory_add_item).

### Request Parameters:

name
: (string) The Name of the new Inventory List

description
: (string) The Description for the Inventory List

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Inventory List

retailer
: (object) The Retailer object contains a single retailer_uuid.

skus
: (array) An empty array that is used to hold SKUs associated with the inventory list. To add SKUs to an Inventory List see [Inventory Add Item](/#product_retailerinventory_add_sku).

num_skus
: (number) The total Number of SKUs per the Catalog

created
: (string) The Created parameter is the date the Catalog was Created.

last_updated
: (string) The Last Updated parameter is the date the Catalog was Last Updated.

name
: (string) The Name the supplier has designated for this Catalog

description
: (string) The Description the supplier has provided for this Catalog

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/inventory-lists/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "name": "New Test Inventory List Name FXu6XvYOGskXhn1v5SAL17IW7AeTImhA",
  "description": "The Description for the New Test Inventory List Name"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/inventory-lists/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    name="New Test Inventory List Name FXu6XvYOGskXhn1v5SAL17IW7AeTImhA" \
    description="The Description for the New Test Inventory List Name"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Create Inventory List
    # POST https://api-sandbox.cruxconnect.com/products/inventory-lists/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/inventory-lists/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    name="New Test Inventory List Name FXu6XvYOGskXhn1v5SAL17IW7AeTImhA" \
    description="The Description for the New Test Inventory List Name")
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
// request Create Inventory List
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/inventory-lists/',
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
    request.write("{\"name\":\"New Test Inventory List Name FXu6XvYOGskXhn1v5SAL17IW7AeTImhA\",\"description\":\"The Description for the New Test Inventory List Name\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
