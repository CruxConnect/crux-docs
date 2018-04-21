---
title: /orders/export/
name: Get Orders Export
position: 6.02
visibility: public
method: post
description: Get an Export of the Order List via an email
right_code: |
  ~~~ json
  {
    "uuids": [
      "1ab8e55f-ea7e-4a58-b7d3-db723272dbbd"
    ]
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "521c8baa-1c44-4ca7-88ce-f4eadba37bc0"
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

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/orders/export/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "uuids": [
    "1ab8e55f-ea7e-4a58-b7d3-db723272dbbd"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/orders/export/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    uuids:="[
  \"1ab8e55f-ea7e-4a58-b7d3-db723272dbbd\"
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
    # POST https://api-sandbox.cruxconnect.com/orders/export/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/orders/export/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    uuids:="[
  \"1ab8e55f-ea7e-4a58-b7d3-db723272dbbd\"
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
        path: '/orders/export/',
        method: 'POST',
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
    request.write("{\"uuids\":[\"1ab8e55f-ea7e-4a58-b7d3-db723272dbbd\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
