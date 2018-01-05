---
title: /api/products/inventory-lists/&ltinventory_list_uuid&gt/remove-skus/
name: Inventory Remove SKU - Retailer
position: 2.13
method: post
description: Remove SKUs from an existing Inventory List for your account
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
Remove SKUs from an existing Inventory List for your account. This allows you to remove SKUs from an Inventory List. By providing your inventory_list_uuid and a list of sku_uuids, you can successfully remove them from the indicated Inventory List.

### Request Parameters:

skus
: (list) The SKUs list parameter holds sku_uuids for all of the SKUs you wish to add to your Inventory List

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
curl -X "POST" "https://stable.projectthanos.com/api/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/remove-skus/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
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
http --json POST 'https://stable.projectthanos.com/api/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/remove-skus/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
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
    # Inventory Remove SKU - Retailer
    # POST https://stable.projectthanos.com/api/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/remove-skus/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/remove-skus/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
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
// request Inventory Remove SKU - Retailer
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/remove-skus/',
        method: 'POST',
        headers: {"Authorization":"Token a0f17278bed479ee719ea890b8caf0329e1f3e5b","Content-Type":"application/json; charset=utf-8"}
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
