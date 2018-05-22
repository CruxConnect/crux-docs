---
title: /orders/tracking/&lt;order_uuid&gt;/&lt;tracking_number&gt;/
name: Update Order Tracking
position: 5.2.2
visibility: public
method: put
description: Update an Order's Tracking number information
right_code: |
  ~~~ json
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
  }
  ~~~
  {: title="Request" }

---
It simply supplies the updated changes to a tracking object. The entire object need not, but can be supplied. All changes that are supplied will be changed, including the tracking_number.

### URL Parameters

order_uuid
: (string) The Universal Unique Identifier for the Order

tracking_number
: (string) The tracking number to be updated

### Request Parameters:

{% include orders/request/tracking_number.md %}

#### Line Item Object:

{% include orders/request/line_item.md %}

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "PUT" "https://api-sandbox.cruxconnect.com/orders/tracking/0e63ac67-7c45-454d-b2ef-bb6b5ed387c3/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "ship_cost": 34.38,
  "tracking": "123mytrack",
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
http --json PUT 'https://api-sandbox.cruxconnect.com/orders/tracking/0e63ac67-7c45-454d-b2ef-bb6b5ed387c3/123mytrack/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
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

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Add Order Tracking - Supplier
    # PUT https://api-sandbox.cruxconnect.com/orders/tracking/0e63ac67-7c45-454d-b2ef-bb6b5ed387c3/

    try:
        response = requests.put(
            url="https://api-sandbox.cruxconnect.com/orders/tracking/0e63ac67-7c45-454d-b2ef-bb6b5ed387c3/123mytrack/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    ship_cost:=34.38 \
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
// request Add Order Tracking - Supplier
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/orders/tracking/0e63ac67-7c45-454d-b2ef-bb6b5ed387c3/123mytrack/',
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
    request.write("{\"tracking\":\"123mytrack\",\"ship_cost\":34.38,\"carrier\":\"UPS\",\"method\":\"Ground\",\"weight\":17.2,\"line_items\":[{\"quantity\":\"1\",\"line_item_uuid\":\"e2c1bcab-43ef-48b8-9aa7-513755a92abc\",\"sku_cost\":\"27\"}]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
