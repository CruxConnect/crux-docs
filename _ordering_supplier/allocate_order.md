---
title: /timp/orders/allocation/319bba9f-71b1-4a93-8abf-67a45b8fdd5c/
name: Allocate Order
position: 6.00
visibility: public
method: put
description: Allocate stock for a Retailer Order
right_code: |
  ~~~ json
  {
    "line_items": [
      {
        "line_item_uuid": "b84ccd3c-88f8-4050-accf-e049163052e3",
        "allocation": {
          "quantity_accepted": "5",
          "quantity_rejected": "0",
          "quantity_backordered": "1",
          "backorder_date": "2019-01-01"
        }
      }
    ]
  }
  ~~~
  {: title="Request" }

  ~~~ json
  [
    {
      "b84ccd3c-88f8-4050-accf-e049163052e3": "Allocated"
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
: (array) ***Required*** The Order Line Items array contains the individual Order Item objects

#### Order Item Object

line_item_uuid
: (string) ***Required*** The line item uuid for the product purchased by the Retailer

allocation
: (object) ***Required*** The Allocation Object parameter includes the quantites accepted, rejected, and backordered.

#### Allocation Object

quantity_accepted
: (integer) ***Required*** The Quantiy Accepted by the supplier

quantity_rejected
: (integer) ***Required*** The Quantity Rejected by the Supplier is the Quantity that they cannot fulfill.

quantity_backordered
: (integer) ***Required*** The Quantity Backordered is the quantity of the order that cannot be shipped because it is currently in a "backordered" state.

backorder_date
: (string) The Date that the Backordered SKU will be available for shipment. String format: yyyy-mmm-ddd

### Response Parameters

line_items
: (array) Array of line item objects

#### Line Item Objects

line_item_uuid
: (string) The Universal Unique Identifier for the Item

quantity_shipped
: (integer) The Quantity of the Item included in the shipment associated with the Tracking Number

supplier_provided_sku_cost
: (decimal) The SKU cost (2 decimal places)

### Expected Response Codes

{% include timp/links/response_codes.md %}

### Expected Response Codes

# Short Description
Allocate stock for a Retailer Order

# Long Description
Allocate stock for a Retailer Order. Essentially accepting the entire order or a portion of the order by providing the order_uuid and providing the order_item_id and associated quantities per the allocation types.


### URL Parameters:

order_uuid
: (string) Universal Unique Identifier for the Order

### Request Parameters:

line_items
: (array) ***Required*** The Order Line Items array contains the individual Order Item objects

#### Order Item Object

line_item_uuid
: (string) ***Required*** The line item uuid for the product purchased by the Retailer

allocation
: (object) ***Required*** The Allocation Object parameter includes the quantites accepted, rejected, and backordered.

#### Allocation Object

quantity_accepted
: (integer) ***Required*** The Quantiy Accepted by the supplier

quantity_rejected
: (integer) ***Required*** The Quantity Rejected by the Supplier is the Quantity that they cannot fulfill.

quantity_backordered
: (integer) ***Required*** The Quantity Backordered is the quantity of the order that cannot be shipped because it is currently in a "backordered" state.

backorder_date
: (string) The Date that the Backordered SKU will be available for shipment. String format: yyyy-mmm-ddd

### Response Parameters

line_items
: (array) Array of line item objects

#### Line Item Objects

line_item_uuid
: (string) The Universal Unique Identifier for the Item

quantity_shipped
: (integer) The Quantity of the Item included in the shipment associated with the Tracking Number

supplier_provided_sku_cost
: (decimal) The SKU cost (2 decimal places)

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "PUT" "https://api-dev.cruxconnect.com/timp/orders/allocation/319bba9f-71b1-4a93-8abf-67a45b8fdd5c/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "line_items": [
    {
      "line_item_uuid": "b84ccd3c-88f8-4050-accf-e049163052e3",
      "allocation": {
        "backorder_date": "2019-01-01",
        "quantity_rejected": "0",
        "quantity_accepted": "5",
        "quantity_backordered": "1"
      }
    }
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json PUT 'https://api-dev.cruxconnect.com/timp/orders/allocation/319bba9f-71b1-4a93-8abf-67a45b8fdd5c/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    line_items:="[
  {
    \"line_item_uuid\": \"b84ccd3c-88f8-4050-accf-e049163052e3\",
    \"allocation\": {
      \"backorder_date\": \"2019-01-01\",
      \"quantity_rejected\": \"0\",
      \"quantity_accepted\": \"5\",
      \"quantity_backordered\": \"1\"
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
    # Allocate Order
    # PUT https://api-dev.cruxconnect.com/timp/orders/allocation/319bba9f-71b1-4a93-8abf-67a45b8fdd5c/

    try:
        response = requests.put(
            url="https://api-dev.cruxconnect.com/timp/orders/allocation/319bba9f-71b1-4a93-8abf-67a45b8fdd5c/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    line_items:="[
  {
    \"line_item_uuid\": \"b84ccd3c-88f8-4050-accf-e049163052e3\",
    \"allocation\": {
      \"backorder_date\": \"2019-01-01\",
      \"quantity_rejected\": \"0\",
      \"quantity_accepted\": \"5\",
      \"quantity_backordered\": \"1\"
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
// request Allocate Order
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/timp/orders/allocation/319bba9f-71b1-4a93-8abf-67a45b8fdd5c/',
        method: 'PUT',
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
    request.write("{\"line_items\":[{\"line_item_uuid\":\"b84ccd3c-88f8-4050-accf-e049163052e3\",\"allocation\":{\"quantity_accepted\":\"5\",\"quantity_rejected\":\"0\",\"quantity_backordered\":\"1\",\"backorder_date\":\"2019-01-01\"}}]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
