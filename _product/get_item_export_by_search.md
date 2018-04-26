---
title: /products/items/search/export/
name: Get Item Export by Search
position: 4.06
visibility: public
method: post
description: Get Item List allows you to return a complete list of items you are interested in.
right_code: |
  ~~~ json
  {
    "item_uuids": [
      "0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017",
      "31adb57c-a40a-4a99-b3d0-3c6ccd8e8941"
    ]
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "export": {
      "uuid": "99f15ad9-d8ac-4f07-8eff-94640d807618"
    }
  }
  ~~~
  {: title="Response" }

---
Get an Export of the Items sent back to the browser or via an email to your email address on file.

The file returned is a comma delimited (.csv)  containing the response parameter data in a flat format.

If there are no skus, then the returned export is a csv file with a simple header (item_id and sku_id) with no underlying values.

### Request Parameters:

item_uuids
: (list) The Item UUIDs parameter provides a list of item_uuids to be exported

### Response Parameters:

uuid
: (string) The Universal Unique Identifier for the Export.

#### Expected Response Codes
{% include links/response_codes.md %}

~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/items/search/export/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "item_uuids": [
    "0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017",
    "31adb57c-a40a-4a99-b3d0-3c6ccd8e8941"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/items/search/export/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    item_uuids:="[
  \"0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017\",
  \"31adb57c-a40a-4a99-b3d0-3c6ccd8e8941\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Item Export by Search
    # POST https://api-sandbox.cruxconnect.com/products/items/search/export/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/items/search/export/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    item_uuids:="[
  \"0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017\",
  \"31adb57c-a40a-4a99-b3d0-3c6ccd8e8941\"
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
// request Get Item Export by Search
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/items/search/export/',
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
    request.write("{\"item_uuids\":[\"0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017\",\"31adb57c-a40a-4a99-b3d0-3c6ccd8e8941\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
