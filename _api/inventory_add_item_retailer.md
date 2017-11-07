---
title: /api/products/inventory-lists/&ltinventory_list_uuid&gt/add-items/
name: Inventory Add Item - Retailer
position: 2.14
type: post
description: Add Items to an existing Inventory List for your account
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


---
Add Items to an existing Inventory List for your account. This allows you to add Items with all associated SKUs to an Inventory List. By providing your inventory_list_uuid and a list of item_uuids, you can successfully add them to the indicated Inventory List. Your username and password are optional as you can send your authorization token to receive this information.

URL Endpoint: /api/products/inventory-lists/\<inventory_list_uuid\>/add-items/

### Request Parameters:

item_uuids
: (list) The Items list parameter holds item_uuids for all of the items you wish to add to your Inventory List

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
curl -X "POST" "https://stable.projectthanos.com/api/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/add-items/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
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
http --json POST 'https://stable.projectthanos.com/api/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/add-items/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
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
    # Inventory Add Item - Retailer
    # POST https://stable.projectthanos.com/api/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/add-items/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/add-items/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
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
// request Inventory Add Item - Retailer
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/products/inventory-lists/c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18/add-items/',
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
