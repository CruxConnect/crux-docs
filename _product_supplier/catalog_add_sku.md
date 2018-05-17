---
title: /products/catalogs/&ltcatalog-uuid&gt/add-skus/
name: Catalog Add SKU
position: 12.06
visibility: public
method: post
description: Add already existing SKUs to a Catalog
right_code: |
  ~~~ json
  {
    "sku_uuids": [
      "12bfdcde-c9f2-4c70-b39c-6b9f5b884c4d"
    ]
  }
  ~~~
  {: title="Request" }


---
Add already existing SKUs to a Catalog for Retailers to access. By providing your catalog_uuid in the URL and array of sku_uuids, you can successfully add them to items previously included in the indicated Catalog.

### URL Parameters

catalog_uuid
: (string) Universal Unique Identifier for the catalog to which the sku will be added

### Request Parameters:

sku_uuids
: (array) The SKU UUIDs parameter holds an array of sku_uuids

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/catalogs/7c973d2d-e888-4aa6-878d-5b62253cf0ea/add-skus/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "sku_uuids": [
    "12bfdcde-c9f2-4c70-b39c-6b9f5b884c4d"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/catalogs/7c973d2d-e888-4aa6-878d-5b62253cf0ea/add-skus/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    sku_uuids:="[
  \"12bfdcde-c9f2-4c70-b39c-6b9f5b884c4d\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Catalog Add SKU
    # POST https://api-sandbox.cruxconnect.com/products/catalogs/7c973d2d-e888-4aa6-878d-5b62253cf0ea/add-skus/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/catalogs/7c973d2d-e888-4aa6-878d-5b62253cf0ea/add-skus/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    sku_uuids:="[
  \"12bfdcde-c9f2-4c70-b39c-6b9f5b884c4d\"
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
// request Catalog Add SKU
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/catalogs/7c973d2d-e888-4aa6-878d-5b62253cf0ea/add-skus/',
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
    request.write("{\"sku_uuids\":[\"12bfdcde-c9f2-4c70-b39c-6b9f5b884c4d\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
