---
title: /orders/tracking/&lt;order_uuid&gt;/
name: Add Order Tracking
position: 5.2.1
visibility: v1
method: post
description: Add a Tracking number to an Order
right_code: |
  ~~~ json
  {
    {
      "tracking": "123mytrack",
      "ship_cost": 34.38,
      "carrier": "UPS",
      "method": "Ground",
      "weight": 17.2,
      "line_items": [
        {
          "quantity": "1",
          "line_item_uuid": "e2c1bcab-43ef-48b8-9aa7-513755a92abc",
          "sku_cost": "27"
        }
      ]
    },
  }
  ~~~
  {: title="Request" }


---
Add a Tracking number to an Order. Essentially adding tracking to the entire order or a portion of the order by providing the order_uuid and providing the tracking, ship_cost, carrier, method, weight, and line_items with item_uuid and quantity.

### URL Parameters

order_uuid
: (string) The Universal Unique Identifier for the Order

### Request Parameters:

{% include v1/orders/request/tracking_number.md %}

#### Line Item Object:

{% include v1/orders/request/line_item.md %}

### Expected Response Codes

{% include v1/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/orders/tracking/0e63ac67-7c45-454d-b2ef-bb6b5ed387c3/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
    "tracking": "123mytrack",
    "ship_cost": 34.38,
    "carrier": "UPS",
    "method": "Ground",
    "weight": 17.2,
    "line_items": [
      {
        "sku_cost": "27",
        "quantity": "1",
        "line_item_uuid": "e2c1bcab-43ef-48b8-9aa7-513755a92abc"
      }
    ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/orders/tracking/0e63ac67-7c45-454d-b2ef-bb6b5ed387c3/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    tracking_numbers:="[
      ship_cost:=34.38 \
      tracking="123mytrack" \
      carrier="UPS" \
      method="Ground" \
      weight:=17.2 \
      line_items:="[
    {
      \"sku_cost\": \"27\",
      \"quantity\": \"1\",
      \"line_item_uuid\": \"e2c1bcab-43ef-48b8-9aa7-513755a92abc\"
    }
  ]"
]"


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Add Order Tracking - Supplier
    # POST https://api-sandbox.cruxconnect.com/orders/tracking/0e63ac67-7c45-454d-b2ef-bb6b5ed387c3/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/orders/tracking/0e63ac67-7c45-454d-b2ef-bb6b5ed387c3/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(
          "
          tracking="123mytrack" \
          ship_cost:=34.38 \
          carrier="UPS" \
          method="Ground" \
          weight:=17.2 \
          line_items:="[
        {
          \"sku_cost\": \"27\",
          \"quantity\": \"1\",
          \"line_item_uuid\": \"e2c1bcab-43ef-48b8-9aa7-513755a92abc\"
        }
      ]"
    "
)
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
        path: '/orders/tracking/0e63ac67-7c45-454d-b2ef-bb6b5ed387c3/',
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
    request.write({\"tracking\":\"123mytrack\",\"ship_cost\":34.38,\"carrier\":\"UPS\",\"method\":\"Ground\",\"weight\":17.2,\"line_items\":[{\"quantity\":\"1\",\"line_item_uuid\":\"e2c1bcab-43ef-48b8-9aa7-513755a92abc\",\"sku_cost\":\"27\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
