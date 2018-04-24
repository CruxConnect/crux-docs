---
title: /products/catalogs/&ltcatalog-uuid&gt/add-items/
name: Catalog Add Item
position: 2.04
visibility: public
method: post
description: Add already existing Items to a Catalog
right_code: |
  ~~~ json
  {
    "item_uuids": [
      "e9e3cc96-515c-46ce-9aa3-c573e92b861b"
    ]
  }
  ~~~
  {: title="Request" }


---
Add already existing Items to a Catalog for Retailers to access. This allows you to add Items to a Catalog with all associated SKUs. By providing your catalog_uuid and a list of item_ids with related data, you can successfully add them to the indicated Catalog.Your username and password are optional as you can send your authorization token to receive this information.

### URL Parameters:

catalog-uuid
: (string) Unique Universal Identifier for the Catalog

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-dev.cruxconnect.com/products/catalogs/1d140dd4-a5f6-4df3-a806-9013a1ef9ef8/add-items/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "item_uuids": [
    "e9e3cc96-515c-46ce-9aa3-c573e92b861b"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-dev.cruxconnect.com/products/catalogs/1d140dd4-a5f6-4df3-a806-9013a1ef9ef8/add-items/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    item_uuids:="[
  \"e9e3cc96-515c-46ce-9aa3-c573e92b861b\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Catalog Add Item
    # POST https://api-dev.cruxconnect.com/products/catalogs/1d140dd4-a5f6-4df3-a806-9013a1ef9ef8/add-items/

    try:
        response = requests.post(
            url="https://api-dev.cruxconnect.com/products/catalogs/1d140dd4-a5f6-4df3-a806-9013a1ef9ef8/add-items/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    item_uuids:="[
  \"e9e3cc96-515c-46ce-9aa3-c573e92b861b\"
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
// request Catalog Add Item
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/products/catalogs/1d140dd4-a5f6-4df3-a806-9013a1ef9ef8/add-items/',
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
    request.write("{\"item_uuids\":[\"e9e3cc96-515c-46ce-9aa3-c573e92b861b\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
