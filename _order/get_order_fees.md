---
title: /timp/orders/&lt;order_uuid&gt;/fees/
name: Get Order Fees
position: 4.04
visibility: public
method: get
description: Get the Fees for an Order.
right_code: |

  ~~~ json
  {
    "retailer_provided_tax": 2.97,
    "retailer_provided_order_fee": 0.99,
    "retailer_provided_shipping_cost": 7.99,
    "retailer_provided_dropship_fee": null,
    "supplier_provided_dropship_fee": null,
    "supplier_provided_order_fee": 0.25,
    "supplier_provided_tax": 1.25,
    "supplier_provided_po_number": null,
    "supplier_provided_order_total": 150,
    "line_items": [
      {
        "line_item_uuid": "0505d71f-4360-4055-b3e8-0caf51c93491",
        "supplier_provided_sku_cost": 0
      }
    ]
  }
  ~~~
  {: title="Response" }

---
Before placing an order, use this call to return the total Fees for the Order. This may be used a number of ways. Perhaps you would like to make sure you are charging enough for an order and would like a "sanity check" on the price before committing to the potential buyer. This API call allows you to get the full, all-inclusive price for the Order.


### Response Parameters:

supplier_provided_drop_ship_fee
: (decimal) Supplier provided drop ship fee (2 decimal positions)

supplier_provided_order_fee
: (decimal) Supplier provided order fee (2 decimal places)

supplier_provided_tax
: (decimal) Supplier provided tax (2 decimal places)

supplier_po_number
: (string) Supplier provided purchase order number

supplier_provided_order_total
: (decimal) Supplier provided (2 decimal places)

line_items
: (array) Array of line item objects

retailer_provided_tax
: (decimal) Retail provided tax (2 decimal places)

retailer_provided_order_fee
: (decimal) Retailer provided fee (2 decimal places)

retailer_provided_shipping_cost
: (decimal) Retailer provided shipping cost (2 decimal places)

retailer_provided_drop_ship_fee
: (decimal) Retail provided drop ship fee (2 decimal places)

#### Line Item Object

line_item_uuid
: (string) Line item universal unique identifier

supplier_provided_sku_cost
: decimal Supplier provide sku cost(2 decimal places)

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/fees/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/fees/' \
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
    # Get Order Fees
    # GET https://api-sandbox.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/fees/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/fees/",
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
// request Get Order Fees
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/fees/',
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
