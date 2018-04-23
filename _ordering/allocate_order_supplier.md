---
title: /orders/allocation/&lgorder-uuid&gt/
name: Allocate Order - Supplier
position: 5.6
visibility: public
method: put
description: Allocate stock for a Retailer Order
right_code: |
  ~~~ json
  {
    "line_items": [
      {
        "line_item_uuid": "d3842ec4-d1f8-4cf1-860b-b9eeb8a35680",
        "allocation": {
          "quantity_accepted": "22",
          "quantity_rejected": "0",
          "quantity_backordered": "0"
        }
      }
    ]
  }
  ~~~
  {: title="Request" }

  ~~~ json
  [
    {
      "d3842ec4-d1f8-4cf1-860b-b9eeb8a35680": "Allocated"
    }
  ]
  ~~~
  {: title="Response" }

---
Allocate stock for a Retailer Order. Essentially accepting the entire order or a portion of the order by providing the order_uuid and providing the order_item_id and associated quantities per the allocation types.

### URL Parameters:

order_uuid
: (string) Universal Unique Identifier for the Order

### Request Parameters:

line_items
: (array) The Order Items array contains the individual Order Item objects

#### Order Item Object

line_item_uuid
: (string) The Order Item ID is the sku_id for the product purchased by the Retailer

allocation
: (object) The Allocation Object parameter includes the quantites accepted, rejected, and backordered.

#### Allocation Object

{% include objects/allocation.md %}

### Response Parameters

Array of allocation objects structured as { uuid: status } key:value pairs where

uuid
: (string) Universal Unique Idenfitier for the allocated item

status
: (string) Status of the allocated Item.  Can be "Allocated", "Backordered", "Cancelled", "Rejected", or "Item Not Found"

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "PUT" "https://api-sandbox.cruxconnect.com/orders/allocation/1ab8e55f-ea7e-4a58-b7d3-db723272dbbd/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "line_items": [
    {
      "line_item_uuid": "d3842ec4-d1f8-4cf1-860b-b9eeb8a35680",
      "allocation": {
        "quantity_backordered": "0",
        "quantity_accepted": "22",
        "quantity_rejected": "0"
      }
    }
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json PUT 'https://api-sandbox.cruxconnect.com/orders/allocation/1ab8e55f-ea7e-4a58-b7d3-db723272dbbd/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    line_items:="[
  {
    \"line_item_uuid\": \"d3842ec4-d1f8-4cf1-860b-b9eeb8a35680\",
    \"allocation\": {
      \"quantity_backordered\": \"0\",
      \"quantity_accepted\": \"22\",
      \"quantity_rejected\": \"0\"
    }
  }
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Allocate Order - Supplier
    # PUT https://api-sandbox.cruxconnect.com/orders/allocation/1ab8e55f-ea7e-4a58-b7d3-db723272dbbd/

    try:
        response = requests.put(
            url="https://api-sandbox.cruxconnect.com/orders/allocation/1ab8e55f-ea7e-4a58-b7d3-db723272dbbd/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    line_items:="[
  {
    \"line_item_uuid\": \"d3842ec4-d1f8-4cf1-860b-b9eeb8a35680\",
    \"allocation\": {
      \"quantity_backordered\": \"0\",
      \"quantity_accepted\": \"22\",
      \"quantity_rejected\": \"0\"
    }
  }
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
// request Allocate Order - Supplier
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/orders/allocation/1ab8e55f-ea7e-4a58-b7d3-db723272dbbd/',
        method: 'PUT',
        headers: {"Authorization":"Token 47d4yfbwymedhiudj384702984nakju4hajh395d","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"line_items\":[{\"line_item_uuid\":\"d3842ec4-d1f8-4cf1-860b-b9eeb8a35680\",\"allocation\":{\"quantity_accepted\":\"22\",\"quantity_rejected\":\"0\",\"quantity_backordered\":\"0\"}}]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
