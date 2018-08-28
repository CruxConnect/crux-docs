---
title: /timp/products/catalogs/&lt;catalog_uuid&gt;/remove-items/
name: Catalog Remove Items
position: 11.05
visibility: public
method: post
description: Remove Items to a Catalog
right_code: |
  ~~~ json
  {
    "item_uuids": [
      "147c1a2d-6a2f-4ee4-b3e5-f8e2ca726f47"
    ]
  }
  ~~~
  {: title="Request" }


---
Remove Items from the specified Catalog for Retailers to access. This allows you to remove Items and all associated SKUs from a Catalog.

### URL Parameters

catalog_uuid
: (string) Universal Unique Identifier for the selected catalog

### Request Parameters:

item_uuids
: (array) The Item UUIDs list parameter holds item_uuids for all of the items you wish to remove from your Catalog

### Expected Response Codes

{% include timp/links/response_codes.md %}

### Expected Response Codes

# Short Description
Remove Items to a Catalog

# Long Description
Remove Items from the specified Catalog for Retailers to access. This allows you to remove Items and all associated SKUs from a Catalog.

### URL Parameters

catalog_uuid
: (string) Universal Unique Identifier for the selected catalog

### Request Parameters:

item_uuids
: (array) The Item UUIDs list parameter holds item_uuids for all of the items you wish to remove from your Catalog

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/timp/products/catalogs/baffb36f-0bdd-46d7-9413-7b8a1cc8fe3e/remove-items/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "item_uuids": [
    "147c1a2d-6a2f-4ee4-b3e5-f8e2ca726f47"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/timp/products/catalogs/baffb36f-0bdd-46d7-9413-7b8a1cc8fe3e/remove-items/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    item_uuids:="[
  \"147c1a2d-6a2f-4ee4-b3e5-f8e2ca726f47\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Catalog Remove Items
    # POST https://api-sandbox.cruxconnect.com/timp/products/catalogs/baffb36f-0bdd-46d7-9413-7b8a1cc8fe3e/remove-items/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/timp/products/catalogs/baffb36f-0bdd-46d7-9413-7b8a1cc8fe3e/remove-items/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    item_uuids:="[
  \"147c1a2d-6a2f-4ee4-b3e5-f8e2ca726f47\"
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
// request Catalog Remove Items
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/products/catalogs/baffb36f-0bdd-46d7-9413-7b8a1cc8fe3e/remove-items/',
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
    request.write("{\"item_uuids\":[\"147c1a2d-6a2f-4ee4-b3e5-f8e2ca726f47\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
