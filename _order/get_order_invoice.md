---
title: /timp/orders/&lt;order_uuid&gt;/invoices/
name: Get Order Invoices
position: 5.2
visibility: public
method: get
description: Get Order attributes
right_code: |
  ~~~ json
  {
    "order_uuid": "319bba9f-71b1-4a93-8abf-67a45b8fdd5c",
    "po_number": "8e5b1ccb-0221-4e26-a343-cd566bfe7419",
    "created_date": "2018-06-28T12:57:30.359784Z",
    "address": {
      "name": "Megan King",
      "business_name": "Black-Rice",
      "address1": "08712 Villarreal Cliffs\nBishopchester, OK 45032",
      "address2": "9652 Richard Plains\nErikamouth, MP 22422-9361",
      "city": "Franklinbury",
      "state": "North Dakota",
      "postal_code": "85254",
      "phone_number": null,
      "country": "USA"
    },
    "sent_to_supplier": false,
    "retailer": {
      "uuid": "ebf3657c-2abb-4aff-be70-69082acc9302",
      "organization_name": "projectthanos",
      "order_submitted_by": null
    },
    "retailer_provided_notes": "Eaque aut inventore itaque commodi est quas laborum.",
    "retailer_provided_fees": {
      "order_fee": null,
      "order_tax": null,
      "shipping_cost": null,
      "dropship_fee": null
    },
    "retailer_provided_order_attributes": null,
    "invoices": [
      {
        "invoice_items": null
      }
    ],
    "line_items": [
      {
        "line_item_uuid": "b84ccd3c-88f8-4050-accf-e049163052e3",
        "status": "Allocated",
        "line_item_designation": "ID: 1 Name: HasTracking",
        "item_uuid": "2aeabb83-938a-4d15-a48a-da84fca11d0e",
        "item_name": "The elementary seed item",
        "sku_uuid": "a7f2cdb3-f84f-463d-91dd-51de21b119b4",
        "sku_id": "q7FSuuTXgawxPxzDs3r",
        "sku_name": "The elementary seed item",
        "quantity_ordered": 5,
        "sku_title_variants": null,
        "product_codes": {
          "upca": null,
          "ean13": null,
          "isbn": null,
          "gtin14": null,
          "asin": null,
          "mpn": null
        },
        "retailer_provided_line_item_notes": null,
        "retailer_provided_sku_cost": 0,
        "supplier": {
          "uuid": "fddc07e7-4383-4e63-929f-f10c3b0864f0",
          "organization_name": "projectzuul",
          "order_submitted_by": null
        },
        "supplier_provided_line_item_notes": null,
        "supplier_provided_attributes": null,
        "tracking": [
          {
            "tracking_number": "t01",
            "shipping_carrier": null,
            "shipping_method": null,
            "shipping_weight": null,
            "shipping_cost": null,
            "shipping_date": null,
            "created_date": null,
            "quantity": 2
          }
        ],
        "allocation": {
          "quantity_ordered": 5,
          "quantity_accepted": 5,
          "quantity_backordered": 1,
          "quantity_rejected": 0,
          "backorder_date": "2019-01-01"
        }
      },
    ]
  }
  ~~~
  {: title="Response" }

---
Get Order attributes

### URL Parameters:

order_uuid
: (string) The Universal Unique Identifier for the order


### Response Parameters:

retailer_provided_notes
: (string) Retailer provided notes

retailer_provided_order_attributes
: (array) An array of retailer provided order attribute objects

line_items
: (array) An array of line item objects


#### Line Item Object

line_item_uuid
: (string) The Universal Unique Identifier for the line item

supplier_provided_notes
: (string) Supplier provided notes

supplier_provided_order_attributes
: (array) An array of supplier provided order attribute objects


#### Attribute Object

attribute_name
: (string) Attribute name

attribute_value
: (string) Attribute value

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/timp/orders/319bba9f-71b1-4a93-8abf-67a45b8fdd5c/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -H 'Cookie: sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/timp/orders/319bba9f-71b1-4a93-8abf-67a45b8fdd5c/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    'Cookie':'sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Order Invoices
    # GET https://api-sandbox.cruxconnect.com/timp/orders/319bba9f-71b1-4a93-8abf-67a45b8fdd5c/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/timp/orders/319bba9f-71b1-4a93-8abf-67a45b8fdd5c/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
                "Cookie": "sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz",
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
// request Get Order Invoices
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/orders/319bba9f-71b1-4a93-8abf-67a45b8fdd5c/',
        method: 'GET',
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
