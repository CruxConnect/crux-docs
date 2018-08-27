---
title: /timp/orders/acknowledge/
name: Acknowlege Order
position: 8.2
visibility: public
method: put
description: Acknowlege Order
right_code: |
  ~~~ json
  {
    "uuids": [
      {
        "order_uuid": "b2cb6ef8-da7a-463e-a7fd-69f0b0ba555e"
      }
    ]
  }
  ~~~
  {: title="Request" }


---
Acknowledge Order

### Request Parameters:

uuids
: (array) An array of order uuid objects

#### Order UUID Object

order_uuid
: (string) Universal Unique Identifier for the order

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "PUT" "https://api-sandbox.cruxconnect.com/timp/orders/acknowledge/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -H 'Cookie: sessionid=itn4tp175a1nwodmxz81o9obsayv9qmi' \
     -d $'{
  "uuids": [
    {
      "order_uuid": "b2cb6ef8-da7a-463e-a7fd-69f0b0ba555e"
    }
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json PUT 'https://api-sandbox.cruxconnect.com/timp/orders/acknowledge/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    'Cookie':'sessionid=itn4tp175a1nwodmxz81o9obsayv9qmi' \
    uuids:="[
  {
    \"order_uuid\": \"b2cb6ef8-da7a-463e-a7fd-69f0b0ba555e\"
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
    # Acknowlege Order
    # PUT https://api-sandbox.cruxconnect.com/timp/orders/acknowledge/

    try:
        response = requests.put(
            url="https://api-sandbox.cruxconnect.com/timp/orders/acknowledge/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
                "Cookie": "sessionid=itn4tp175a1nwodmxz81o9obsayv9qmi",
            },
            data=json.dumps(    uuids:="[
  {
    \"order_uuid\": \"b2cb6ef8-da7a-463e-a7fd-69f0b0ba555e\"
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
// request Acknowlege Order
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/orders/acknowledge/',
        method: 'PUT',
        headers: {"Authorization":"Token 1234567890","Content-Type":"application/json; charset=utf-8","Cookie":"sessionid=itn4tp175a1nwodmxz81o9obsayv9qmi"}
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
    request.write("{\"uuids\":[{\"order_uuid\":\"b2cb6ef8-da7a-463e-a7fd-69f0b0ba555e\"}]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
