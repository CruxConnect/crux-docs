---
title: /timp/orders/&lt;order_uuid&gt/invoices/
name: Update Order Invoices
position: 5.2.3
visibility: public
method: post
description: Update Order attributes
right_code: |
  ~~~ json
  {
    "invoice_number": "invoice-01",
    "line_items": [
      {
        "line_item_uuid": "0505d71f-4360-4055-b3e8-0caf51c93491",
        "quantity_invoiced": 1,
        "supplier_provided_sku_cost": 47.98
      }
    ],
    "supplier_provided_drop_ship_fee": 0.84,
    "supplier_provided_order_fee": 1.24,
    "supplier_provided_tax": 2.83,
    "supplier_provided_order_total": 348.92,
    "supplier_provided_shipping_cost": 5.03
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "invoice_uuid": "57451425-1af0-4e12-a87e-c02569f8358a"
  }
  ~~~
  {: title="Response" }

---
Update Order attributes

### URL Parameters:

order_uuid
: (string) The Universal Unique Identifier for the order


### Request Parameters:

invoice_number
: (string) **Required** Invoice number

line_items
: (array) An array of line item objects

supplier_provided_drop_ship_fee
: (decimal) Supplier provided dropship fee (2 decimal places)

supplier_provided_order_fee
: (decimal) Supplier provided order fee  (2 decimal places)

supplier_provided_tax
: (decimal) Supplier provided tax (2 decimal places)

supplier_provided_order_total
: (decimal) Supplier provided order total (2 decimal places)

supplier_provided_shipping_cost
: (decimal) Supplier provided shipping cost (2 decimal places)


#### Line Item Object

line_item_uuid
: (string) **Required** The Universal Unique Identifier for the line item

quantity_invoiced
: (integer) Quantity invoiced

supplier_provided_sku_cost
: (decimal) Supplier provided SKU cost (2 decimal places)


#### Attribute Object

attribute_name
: (string) Attribute name

attribute_value
: (string) Attribute value

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-dev.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/invoices/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -H 'Cookie: sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz' \
     -d $'{
  "line_items": [
    {
      "supplier_provided_sku_cost": 47.98,
      "line_item_uuid": "0505d71f-4360-4055-b3e8-0caf51c93491",
      "quantity_invoiced": 1
    }
  ],
  "supplier_provided_order_fee": 1.24,
  "supplier_provided_drop_ship_fee": 0.84,
  "supplier_provided_order_total": 348.92,
  "supplier_provided_shipping_cost": 5.03,
  "invoice_number": "invoice-01",
  "supplier_provided_tax": 2.83
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-dev.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/invoices/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    'Cookie':'sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz' \
    line_items:="[
  {
    \"supplier_provided_sku_cost\": 47.98,
    \"line_item_uuid\": \"0505d71f-4360-4055-b3e8-0caf51c93491\",
    \"quantity_invoiced\": 1
  }
]" \
    supplier_provided_order_fee:=1.24 \
    supplier_provided_drop_ship_fee:=0.84 \
    supplier_provided_order_total:=348.92 \
    supplier_provided_shipping_cost:=5.03 \
    invoice_number="invoice-01" \
    supplier_provided_tax:=2.83

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Update Order Invoices
    # POST https://api-dev.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/invoices/

    try:
        response = requests.post(
            url="https://api-dev.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/invoices/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
                "Cookie": "sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz",
            },
            data=json.dumps(    line_items:="[
  {
    \"supplier_provided_sku_cost\": 47.98,
    \"line_item_uuid\": \"0505d71f-4360-4055-b3e8-0caf51c93491\",
    \"quantity_invoiced\": 1
  }
]" \
    supplier_provided_order_fee:=1.24 \
    supplier_provided_drop_ship_fee:=0.84 \
    supplier_provided_order_total:=348.92 \
    supplier_provided_shipping_cost:=5.03 \
    invoice_number="invoice-01" \
    supplier_provided_tax:=2.83)
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
// request Update Order Invoices
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/invoices/',
        method: 'POST',
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
    request.write("{\"invoice_number\":\"invoice-01\",\"line_items\":[{\"line_item_uuid\":\"0505d71f-4360-4055-b3e8-0caf51c93491\",\"quantity_invoiced\":1,\"supplier_provided_sku_cost\":47.98}],\"supplier_provided_drop_ship_fee\":0.84,\"supplier_provided_order_fee\":1.24,\"supplier_provided_tax\":2.83,\"supplier_provided_order_total\":348.92,\"supplier_provided_shipping_cost\":5.03}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
