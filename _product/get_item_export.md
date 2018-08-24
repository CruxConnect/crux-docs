---
title: /products/items/export/
name: Get Item Export
position: 3.04
visibility: public
method: post
description: Get Item Export allows you to export the item you are interested.

right_code: |
  ~~~ json
  {
    "item_uuids": [
      "5a5fe856-a4bd-4dd2-ac5e-e3c9c29e5ed4"
    ]
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "export": {
      "uuid": "b039dcf4-3509-49f2-a86e-64df0dc51aba"
    }
  }
  ~~~
  {: title="Response" }

---
Get Item Export allows you to export the item via email to your email address on file

This API call, like other “Export” calls, will send an email to your email address. That is, the email address linked to your user_uuid. The Item Details will be attached to the email as as a comma-delimited (.csv) file.

If there are no skus, then the returned export is a csv file with a simple header (item_id and sku_id) with no underlying values.

### Request Parameters:

item_uuids
: (array) The Item UUIDs parameter provides a list of item_uuids to be exported

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Item

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/items/export/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "item_uuids": [
    "5a5fe856-a4bd-4dd2-ac5e-e3c9c29e5ed4"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/items/export/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    item_uuids:="[
  \"5a5fe856-a4bd-4dd2-ac5e-e3c9c29e5ed4\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Item Export
    # POST https://api-sandbox.cruxconnect.com/products/items/export/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/items/export/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    item_uuids:="[
  \"5a5fe856-a4bd-4dd2-ac5e-e3c9c29e5ed4\"
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
// request Get Item Export
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/items/export/',
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
    request.write("{\"item_uuids\":[\"5a5fe856-a4bd-4dd2-ac5e-e3c9c29e5ed4\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
