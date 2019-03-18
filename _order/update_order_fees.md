---
title: /timp/orders/&lt;order_uuid&gt;/fees/
name: Update Order Fees
position: 4.05
visibility: public
method: post
description: Update the Fees for an Order.
right_code: |
  ~~~ json
  {
    "supplier_provided_dropship_fee": 0.86,
    "supplier_provided_order_fee": 0.25,
    "supplier_provided_tax": 1.25,
    "supplier_provided_po_number": "8e5b1ccb-0221-4e26-a343-cd566bfe7419",
    "supplier_provided_order_total": 150
  }
  ~~~
  {: title="Request" }


---
Allows supplier and retailer to specify their respective order fees.

### URL Parameters

order_uuid
: (string) Order Univeral Unique Identifier

### Request Parameters:

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
curl -X "POST" "https://api-sandbox.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/fees/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "supplier_provided_po_number": "8e5b1ccb-0221-4e26-a343-cd566bfe7419",
  "supplier_provided_dropship_fee": 0.86,
  "supplier_provided_order_fee": 0.25,
  "supplier_provided_order_total": 150,
  "supplier_provided_tax": 1.25
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/fees/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    supplier_provided_po_number="8e5b1ccb-0221-4e26-a343-cd566bfe7419" \
    supplier_provided_dropship_fee:=0.86 \
    supplier_provided_order_fee:=0.25 \
    supplier_provided_order_total:=150 \
    supplier_provided_tax:=1.25

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Update Order Fees
    # POST https://api-sandbox.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/fees/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/fees/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    supplier_provided_po_number="8e5b1ccb-0221-4e26-a343-cd566bfe7419" \
    supplier_provided_dropship_fee:=0.86 \
    supplier_provided_order_fee:=0.25 \
    supplier_provided_order_total:=150 \
    supplier_provided_tax:=1.25)
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
// request Update Order Fees
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/fees/',
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
    request.write("{\"supplier_provided_dropship_fee\":0.86,\"supplier_provided_order_fee\":0.25,\"supplier_provided_tax\":1.25,\"supplier_provided_po_number\":\"8e5b1ccb-0221-4e26-a343-cd566bfe7419\",\"supplier_provided_order_total\":150}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
