---
title: /products/inventory-lists/&ltinventory_list_uuid&gt/add-skus/
name: Inventory Add SKU
position: 2.12
method: post
description: Add SKUs to an existing Inventory List for your account
right_code: |
  ~~~ json
  {
    "sku_uuids": [
      "9060814c-9feb-4a3e-958c-cb26d537cffc",
      "12009d4d-6206-4811-9934-10e6016769e8"
    ]
  }
  ~~~
  {: title="Request" }

---
Add SKUs to an existing Inventory List for your account. This allows you to add SKUs to an Inventory List. By providing your inventory_list_uuid and a list of sku_uuids, you can successfully add them to the indicated Inventory List.

### Request Parameters:

sku_uuids
: (list) The SKU UUIDs list parameter holds sku_uuids for all of the SKUs you wish to add to your Inventory List

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 405  | Method Not Allowed     | Generally, the HTTP verb does not match the intended API call                |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/add-skus/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "sku_uuids": [
    "9060814c-9feb-4a3e-958c-cb26d537cffc",
    "12009d4d-6206-4811-9934-10e6016769e8"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/add-skus/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    sku_uuids:="[
  \"9060814c-9feb-4a3e-958c-cb26d537cffc\",
  \"12009d4d-6206-4811-9934-10e6016769e8\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Inventory Add SKU
    # POST https://api-sandbox.cruxconnect.com/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/add-skus/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/add-skus/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    sku_uuids:="[
  \"9060814c-9feb-4a3e-958c-cb26d537cffc\",
  \"12009d4d-6206-4811-9934-10e6016769e8\"
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
// request Inventory Add SKU
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/add-skus/',
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
    request.write("{\"sku_uuids\":[\"9060814c-9feb-4a3e-958c-cb26d537cffc\",\"12009d4d-6206-4811-9934-10e6016769e8\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
