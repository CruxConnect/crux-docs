---
title: /orders/fees/
name: Get Order Fees - Retailer
position: 3.04
method: post
description: Get the Fees for a potential Order.
right_code: |
  ~~~ json
  {
    "skus": [
      {
        "quantity": 5,
        "sku_id": "12345e-47a",
        "supplier_id": "25432a-fus814-as79asf-askjlu"
      },
      {
        "quantity": 3,
        "sku_id": "224315f-53a",
        "supplier_id": "25432a-fus814-as79asf-askjlu"
      }
    ]
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "estimated_shipping_cost": 27.37,
    "drop_ship_fee": 5.00,
    "order_fee": 47.50
  }
  ~~~
  {: title="Response" }

---
Before placing an order, use this call to return the total Fees for the Order. This may be used a number of ways. Perhaps you would like to make sure you are charging enough for an order and would like a "sanity check" on the price before committing to the potential buyer. This API call allows you to get the full, all-inclusive price for the Order.

### Request Parameters:

#### Required:

skus
: (list) The list of SKUs ordered including the SKU ID and Quantity per SKU

##### SKU Object:

sku_id
: (string) The SKU ID is the SKU provided by the supplier which identifies that product you are purchasing

quantity
: (number) The Quantity ordered of the SKU ID

supplier_id
: (string) The Supplier ID is the Identifier for the supplier. This is used to help determine the origin of the sku_id.

#### Optional:

address
: (object) The Address object containing name, business name, address line 1, address line 2, city, state, postal code

shipping_carrier
: (string) The Shipping Carrier to deliver the order

shipping_method
: (string) The Shipping Method used by the Shipping Carrier to deliver the order

##### Address Object:

name
: (string) The Name associated with the Address

business_name
: (string) The Business Name associated with the Address

address1
: (string) The First line of the Address

address2
: (string) The Second line of the Address. If an apartment or suite, that information should be entered in this parameter.

city
: (string) The City associated with the Address

state
: (string) The State associated with the Address

postal_code
: (number) The Zip Code / Postal Code associated with the Address

### Response Parameters:

estimated_shipping_cost
: (number) The Estimated Shipping Cost of the Order

drop_ship_fee
: (number) The total Drop Ship Fee for the Order

per_order_fee
: (number) The Per Order Fee for the Order

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl -X "POST" "https:/.cruxconnect.com/orders/fees/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "skus": [
    {
      "quantity": 5,
      "sku_id": ""
    },
    {
      "quantity": 3,
      "sku_id": ""
    }
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https:/.cruxconnect.com/orders/fees/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8' \
    skus:="[
  {
    \"quantity\": 5,
    \"sku_id\": \"\"
  },
  {
    \"quantity\": 3,
    \"sku_id\": \"\"
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
    # Get Order Fees - Retailer
    # POST https:/.cruxconnect.com/orders/fees/

    try:
        response = requests.post(
            url="https:/.cruxconnect.com/orders/fees/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    skus:="[
  {
    \"quantity\": 5,
    \"sku_id\": \"\"
  },
  {
    \"quantity\": 3,
    \"sku_id\": \"\"
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
// request Get Order Fees - Retailer
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api.cruxconnect.com',
        port: '443',
        path: '/orders/fees/',
        method: 'POST',
        headers: {"Authorization":"Token a0f17278bed479ee719ea890b8caf0329e1f3e5b","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"skus\":[{\"quantity\":5,\"sku_id\":\"\"},{\"quantity\":3,\"sku_id\":\"\"}]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
