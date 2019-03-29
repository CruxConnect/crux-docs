---
title: /timp/products/skus/inventory/
name: Update sku inventory
position: 12.10
visibility: public
method: post
description: Update a single sku's inventory.
right_code: |
  ~~~ json
  {
    "sku_id": "xkuOwSQ3utl",
    "quantity_in_stock": 3
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "message": "success"
  }
  ~~~
  {: title="Response" }

---
Update a single sku's inventory. Valid fields to update are inventory related: "quantity_in_stock", "quantity_on_backorder", "restrictions". Valid identifiers are sku_id, upca, ean13, gtin14, isbn.


### Request Parameters:

sku_id (or upca, ean13, gtin14, isbn)
: (string) The identifier for the sku as provided by the supplier.

quantity_in_stock
: (int) Quantity of the SKU in stock

quantity_on_backorder
: (int) Quantity of the SKU on backorder

restrictions
: (string) discontd or tmpunavail

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-dev.cruxconnect.com/timp/products/skus/inventory/" \
     -H 'Authorization: Token 1083e3ec5c40b36fd663ba925bc8d864061463e2' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -H 'Cookie: sessionid=0go3ewc40dk7rlevmdziljl3lf3wxpid' \
     -d $'{
  "quantity_in_stock": 3,
  "sku_id": "xkuOwSQ3utl"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-dev.cruxconnect.com/timp/products/skus/inventory/' \
    'Authorization':'Token 1083e3ec5c40b36fd663ba925bc8d864061463e2' \
    'Content-Type':'application/json; charset=utf-8' \
    'Cookie':'sessionid=0go3ewc40dk7rlevmdziljl3lf3wxpid' \
    quantity_in_stock:=3 \
    sku_id="xkuOwSQ3utl"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Update sku inventory
    # POST https://api-dev.cruxconnect.com/timp/products/skus/inventory/

    try:
        response = requests.post(
            url="https://api-dev.cruxconnect.com/timp/products/skus/inventory/",
            headers={
                "Authorization": "Token 1083e3ec5c40b36fd663ba925bc8d864061463e2",
                "Content-Type": "application/json; charset=utf-8",
                "Cookie": "sessionid=0go3ewc40dk7rlevmdziljl3lf3wxpid",
            },
            data=json.dumps(    quantity_in_stock:=3 \
    sku_id="xkuOwSQ3utl")
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
// request Update sku inventory
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/timp/products/skus/inventory/',
        method: 'POST',
        headers: {"Authorization":"Token 1083e3ec5c40b36fd663ba925bc8d864061463e2","Content-Type":"application/json; charset=utf-8","Cookie":"sessionid=0go3ewc40dk7rlevmdziljl3lf3wxpid"}
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
    request.write("{\"sku_id\":\"xkuOwSQ3utl\",\"quantity_in_stock\":3}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
