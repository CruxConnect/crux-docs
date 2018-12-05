---
title: /timp/orders/tracking/&lt;order_uuid&gt;/
name: Add Order Tracking - Supplier
position: 5.2.1
visibility: public
method: post
description: Add a Tracking number or multiple Tacking numbers to an Order.
right_code: |
  ~~~ json
  {
    "tracking_number": "t01",
    "line_items": [
      {
        "line_item_uuid": "71b8b807-3c6b-49c8-91dd-5798896f5253",
        "quantity_shipped": 2,
        "supplier_provided_sku_cost": 13.98
      }
    ],
    "package_attributes": [
      {
        "attribute_name": "package level attribute name",
        "attribute_value": "package level attribute value"
      }
    ]
  }
  ~~~
  {: title="Request" }


---
Add a Tracking number or multiple Tacking numbers to an Order. Essentially adding tracking to the entire order or a portion of the order by providing the order_uuid and providing the tracking, ship_cost, carrier, method, weight, and line_items with item_uuid and quantity.

### URL Parameters

order_uuid
: (string) The Universal Unique Identifier for the Order

### Request Parameters:

tracking_number
: (string) ***Required*** Order tracking number

supplier_provided_carrier
: (string) Supplier provided carrier

supplier_provided_method
: (string) Supplier provided shipping method

package_weight
: (decimal) Package weight

package_ship_cost
: (decimal) Package shipping cost (2 decimal places)

package_ship_date
: (string) Package ship date

line_items
: (array) ***Required*** An array of line item objects

package_attributes
: (array) Supplier provided array of key/value attributes for the package

#### Line Item Object

line_item_uuid
: (string) ***Required*** The Universal Unique Identifier for the line item

quantity_shipped
: (integer) ***Required*** Quantity shipped

supplier_provided_sku_cost
: (decimal) Supplier provided SKU cost (2 decimal places)

### Response Parameters

package_uuid
: (string) Package Universal Unique Identifier

### Expected Response Codes

{% include timp/links/response_codes.md %}

~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/timp/orders/tracking/25d6eb53-e5c0-4019-8cf4-7330f1894e41/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "line_items": [
    {
      "quantity_shipped": 2,
      "line_item_uuid": "71b8b807-3c6b-49c8-91dd-5798896f5253",
      "supplier_provided_sku_cost": 13.98
    }
  ],
  "tracking_number": "t01"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/timp/orders/tracking/25d6eb53-e5c0-4019-8cf4-7330f1894e41/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    line_items:="[
  {
    \"quantity_shipped\": 2,
    \"line_item_uuid\": \"71b8b807-3c6b-49c8-91dd-5798896f5253\",
    \"supplier_provided_sku_cost\": 13.98
  }
]" \
    tracking_number="t01"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Add Order Tracking - Supplier
    # POST https://api-sandbox.cruxconnect.com/timp/orders/tracking/25d6eb53-e5c0-4019-8cf4-7330f1894e41/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/timp/orders/tracking/25d6eb53-e5c0-4019-8cf4-7330f1894e41/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    line_items:="[
  {
    \"quantity_shipped\": 2,
    \"line_item_uuid\": \"71b8b807-3c6b-49c8-91dd-5798896f5253\",
    \"supplier_provided_sku_cost\": 13.98
  }
]" \
    tracking_number="t01")
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
// request Add Order Tracking - Supplier
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/orders/tracking/25d6eb53-e5c0-4019-8cf4-7330f1894e41/',
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
    request.write("{\"tracking_number\":\"t01\",\"line_items\":[{\"line_item_uuid\":\"71b8b807-3c6b-49c8-91dd-5798896f5253\",\"quantity_shipped\":2,\"supplier_provided_sku_cost\":13.98}]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
