---
title: /orders/cancel/
name: Cancel Order
position: 5.7
visibility: public
method: patch
description: Cancel a pending Order (for Retailers)
right_code: |
  ~~~ json
  {
    "order_uuid": "54a31ec5-b0be-4a92-af4c-1b75fe8e6e29",
    "skus": [
      {
        "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f"
      }
    ]
  }
  ~~~
  {: title="Request" }


---
Cancel a pending Order. Granted that the supplier(s) can accept a cancellation, your request to cancel an order is sent to the pertinent supplier(s).


### Request Parameters:

auth_token
: (string) The Authentication Token you were given with the "Login" API call

order_uuid
: (string) The Universal Unique Identifier for the Order which you intend to cancel

skus
: (list) The list of SKUs ordered including the supplier_uuid, sku_id and quantity per SKU

#### SKU Object:

{% include objects/sku.md %}

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "PATCH" "https://api-sandbox.cruxconnect.com/orders/cancel/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "skus": [
    {
      "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f"
    }
  ],
  "order_uuid": "54a31ec5-b0be-4a92-af4c-1b75fe8e6e29"
}'

~~~
{: title="Curl" }

~~~ bash
http --json PATCH 'https://api-sandbox.cruxconnect.com/orders/cancel/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    skus:="[
  {
    \"supplier_uuid\": \"757ce28d-fbd6-4b9f-8051-f847482e169f\"
  }
]" \
    order_uuid="54a31ec5-b0be-4a92-af4c-1b75fe8e6e29"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Cancel Order
    # PATCH https://api-sandbox.cruxconnect.com/orders/cancel/

    try:
        response = requests.patch(
            url="https://api-sandbox.cruxconnect.com/orders/cancel/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    skus:="[
  {
    \"supplier_uuid\": \"757ce28d-fbd6-4b9f-8051-f847482e169f\"
  }
]" \
    order_uuid="54a31ec5-b0be-4a92-af4c-1b75fe8e6e29")
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
// request Cancel Order
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/orders/cancel/',
        method: 'PATCH',
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
    request.write("{\"order_uuid\":\"54a31ec5-b0be-4a92-af4c-1b75fe8e6e29\",\"skus\":[{\"supplier_uuid\":\"757ce28d-fbd6-4b9f-8051-f847482e169f\"}]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
