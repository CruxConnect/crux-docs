---
title: /timp/orders/items/cancel/&lt;order_item_uuid&gt;/reject/
name: Reject Order Item Cancelation
position: 5.2.7
visibility: public
method: patch
description: Reject Order cancelation
right_code: |
  ~~~ json

  ~~~
  {: title="Request" }


---
Reject Order cancelation

### URL Parameters:

order_item_uuid
: (string) Universal Unique Identifier for the canceled order

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "PATCH" "https://api-dev.cruxconnect.com/timp/orders/items/cancel/4efca041-22e1-4e35-96d1-8495273a5868/reject/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Cookie: sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz'

~~~
{: title="Curl" }

~~~ bash
http PATCH 'https://api-dev.cruxconnect.com/timp/orders/items/cancel/4efca041-22e1-4e35-96d1-8495273a5868/reject/' \
    'Authorization':'Token 1234567890' \
    'Cookie':'sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Reject Order Item Cancelation
    # PATCH https://api-dev.cruxconnect.com/timp/orders/items/cancel/4efca041-22e1-4e35-96d1-8495273a5868/reject/

    try:
        response = requests.patch(
            url="https://api-dev.cruxconnect.com/timp/orders/items/cancel/4efca041-22e1-4e35-96d1-8495273a5868/reject/",
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
// request Reject Order Item Cancelation
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/timp/orders/items/cancel/4efca041-22e1-4e35-96d1-8495273a5868/reject/',
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
