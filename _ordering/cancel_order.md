---
title: /api/orders/cancel/
name: Cancel Order
position: 3.06
method: patch
description: Cancel a pending Order (for Retailers)
right_code: |
  ~~~ json
  {
    "order_uuid": "358cd9ec-de30-45c5-b12b-5e4f78037645"
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
: (list) The list of SKUs ordered including the supplier_id, sku_id and quantity per SKU

#### SKU Object:

supplier_id
: (string) The Supplier Identifier is the ID associated with the Supplier providing the SKU

sku_id
: (string) The SKU ID is the SKU provided by the supplier which identifies that product you are purchasing

quantity
: (number) The Quantity ordered of the SKU ID

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 204  | No Content             | The API call was received and the order cancel request is now pending        |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl -X "PATCH" "https://api.cruxconnect.com/api/orders/cancel/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "order_uuid": "358cd9ec-de30-45c5-b12b-5e4f78037645"
}'

~~~
{: title="Curl" }

~~~ bash
http --json PATCH 'https://api.cruxconnect.com/api/orders/cancel/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8' \
    order_uuid="358cd9ec-de30-45c5-b12b-5e4f78037645"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Cancel Order
    # PATCH https://api.cruxconnect.com/api/orders/cancel/

    try:
        response = requests.patch(
            url="https://api.cruxconnect.com/api/orders/cancel/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    order_uuid="358cd9ec-de30-45c5-b12b-5e4f78037645")
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
        hostname: 'api.cruxconnect.com',
        port: '443',
        path: '/api/orders/cancel/',
        method: 'PATCH',
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
    request.write("{\"order_uuid\":\"358cd9ec-de30-45c5-b12b-5e4f78037645\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
