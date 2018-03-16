---
title: /products/items/search/export/
name: Get Item Export by Search
position: 2.22
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
Get Item List allows you to return a complete list of items you are interested in.

### Request Parameters:

item_uuids
: (list) The Item UUIDs parameter provides a list of item_uuids to be exported

### Response Parameters:

export
: (object) The export object contains a single key and value pair of uuid and it's value

uuid
: (string) The Universal Unique Identifier for the Export. Note: In the case of no results in the search the key "uuid" and it's accompanying value will not be displayed at all. (e.g. {"export": {}})

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 405  | Method Not Allowed     | Generally, the HTTP verb is not correct for the intended call                |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


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
