---
title: /timp/orders/export/
name: Get Orders Export
position: 4.02
visibility: public
method: post
description: Get an Export of the Order List via an email
right_code: |
  ~~~ json
  {
    "uuids": [
      "319bba9f-71b1-4a93-8abf-67a45b8fdd5c"
    ]
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "dccef0e0-52ff-4704-a279-3e5b0f92990e"
  }
  ~~~
  {: title="Response" }

---
Get an Export of the Orders via an email to your email address on file.

This API call, like other "Export" calls, will send an email to your email address. That is, the email address linked to your user_uuid. The Order Details will be attached to the email as as a comma-delimited (.csv) file.

We also provide an Export uuid in response to this call.

### Request Parameters:

uuids
: (array) Array of Universal Unique Identifiers for Export

### Response Parameters:

uuid
: (string) The Universal Unique Identifier for the Export

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/timp/orders/export/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "uuids": [
    "319bba9f-71b1-4a93-8abf-67a45b8fdd5c"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/timp/orders/export/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    uuids:="[
  \"319bba9f-71b1-4a93-8abf-67a45b8fdd5c\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Orders Export
    # POST https://api-sandbox.cruxconnect.com/timp/orders/export/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/timp/orders/export/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    uuids:="[
  \"319bba9f-71b1-4a93-8abf-67a45b8fdd5c\"
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
// request Get Orders Export
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/orders/export/',
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
    request.write("{\"uuids\":[\"319bba9f-71b1-4a93-8abf-67a45b8fdd5c\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
