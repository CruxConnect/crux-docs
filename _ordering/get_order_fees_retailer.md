---
title: /orders/fees/
name: Get Order Fees - Retailer
position: 6.04
visibility: public
method: post
description: Get the Fees for a potential Order.
right_code: |
  ~~~ json
  {
    "skus": [
      {
        "quantity": 5,
        "sku_id": "000078"
      }
    ]
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "estimated_shipping_cost": 0,
    "drop_ship_fee": 0,
    "order_fee": 0
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

#### Optional:

address
: (object) The Address object containing name, business name, address line 1, address line 2, city, state, postal code

shipping_carrier
: (string) The Shipping Carrier to deliver the order

shipping_method
: (string) The Shipping Method used by the Shipping Carrier to deliver the order

##### Address Object:

{% include objects/address_business.md %}

### Response Parameters:

estimated_shipping_cost
: (number) The Estimated Shipping Cost of the Order

drop_ship_fee
: (number) The total Drop Ship Fee for the Order

per_order_fee
: (number) The Per Order Fee for the Order

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/orders/fees/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "skus": [
    {
      "quantity": 5,
      "sku_id": "000078"
    }
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/orders/fees/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    skus:="[
  {
    \"quantity\": 5,
    \"sku_id\": \"000078\"
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
    # POST https://api-sandbox.cruxconnect.com/orders/fees/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/orders/fees/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    skus:="[
  {
    \"quantity\": 5,
    \"sku_id\": \"000078\"
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
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/orders/fees/',
        method: 'POST',
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
    request.write("{\"skus\":[{\"quantity\":5,\"sku_id\":\"000078\"}]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
