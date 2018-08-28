---
title: /timp/orders/cancel/&lt;order_uuid&gt;/reject/
name: Reject Order Cancelation
position: 5.2.5
visibility: public
method: patch
description: Reject Order cancelation
right_code: |


---
Reject Order cancelation

### URL Parameters:

order_uuid
: (string) Universal Unique Identifier for the canceled order

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "PATCH" "https://api-dev.cruxconnect.com/timp/orders/cancel/3f756137-f575-4337-b61f-d55b917b146b/reject/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Cookie: sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz'

~~~
{: title="Curl" }

~~~ bash
http PATCH 'https://api-dev.cruxconnect.com/timp/orders/cancel/3f756137-f575-4337-b61f-d55b917b146b/reject/' \
    'Authorization':'Token 1234567890' \
    'Cookie':'sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Reject Order Cancelation
    # PATCH https://api-dev.cruxconnect.com/timp/orders/cancel/3f756137-f575-4337-b61f-d55b917b146b/reject/

    try:
        response = requests.patch(
            url="https://api-dev.cruxconnect.com/timp/orders/cancel/3f756137-f575-4337-b61f-d55b917b146b/reject/",
            headers={
                "Authorization": "Token 1234567890",
                "Cookie": "sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz",
            },
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
// request Reject Order Cancelation
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/timp/orders/cancel/3f756137-f575-4337-b61f-d55b917b146b/reject/',
        method: 'PATCH',
        headers: {"Authorization":"Token 1234567890","Cookie":"sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz"}
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
    request.write("")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
