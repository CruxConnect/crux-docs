---
title: /timp/orders/items/cancel/&lt;order_item_uuid&gt;/confirm/
name: Cancel Order Item
position: 5.2.6
visibility: public
method: patch
description: Cancel Order
right_code: |

---
Cancel Order

### URL Parameters

order_item_uuid
: (string) Universal Unique Identifier for the canceled item

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "PATCH" "https://api-dev.cruxconnect.com/timp/orders/items/cancel/2350a349-2441-4c32-b7f6-99b7e4540b94/confirm/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -H 'Cookie: sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json PATCH 'https://api-dev.cruxconnect.com/timp/orders/items/cancel/2350a349-2441-4c32-b7f6-99b7e4540b94/confirm/' \
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
    # Cancel Order Item
    # PATCH https://api-dev.cruxconnect.com/timp/orders/items/cancel/2350a349-2441-4c32-b7f6-99b7e4540b94/confirm/

    try:
        response = requests.patch(
            url="https://api-dev.cruxconnect.com/timp/orders/items/cancel/2350a349-2441-4c32-b7f6-99b7e4540b94/confirm/",
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
// request Cancel Order Item
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/timp/orders/items/cancel/2350a349-2441-4c32-b7f6-99b7e4540b94/confirm/',
        method: 'PATCH',
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
