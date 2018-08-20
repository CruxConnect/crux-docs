---
title: /products/catalogs/&ltcatalog-uuid&gt/remove-skus/
name: Catalog Remove SKU
position: 12.08
visibility: v1
method: post
description: Remove SKUs from a Catalog
right_code: |
  ~~~ json
  {
    "sku_uuids": [
      "fcf57d87-19ae-46ad-adea-aad17ccb2d15"
    ]
  }
  ~~~
  {: title="Request" }


---
Remove SKUs from a Catalog for Retailers to access. This allows you to remove SKUs from a Catalog. By providing your catalog_uuid and a list of sku_uuids, you can successfully remove them from the indicated Catalog.Your username and password are optional as you can send your authorization token to receive this information.

### URL Parameters

catalog-uuid
: (string) Unique Universal Identifier for the Catalog

### Request Parameters:

sku_uuids
: (array) Array of SKU uuid(s) for all of the SKUs you wish to remove from your Catalog

### Expected Response Codes

{% include v1/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/catalogs/7c973d2d-e888-4aa6-878d-5b62253cf0ea/remove-skus/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "sku_uuids": [
    "fcf57d87-19ae-46ad-adea-aad17ccb2d15"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/catalogs/7c973d2d-e888-4aa6-878d-5b62253cf0ea/remove-skus/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    sku_uuids:="[
  \"fcf57d87-19ae-46ad-adea-aad17ccb2d15\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Catalog Remove SKU
    # POST https://api-sandbox.cruxconnect.com/products/catalogs/7c973d2d-e888-4aa6-878d-5b62253cf0ea/remove-skus/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/catalogs/7c973d2d-e888-4aa6-878d-5b62253cf0ea/remove-skus/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    sku_uuids:="[
  \"fcf57d87-19ae-46ad-adea-aad17ccb2d15\"
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
// request Catalog Remove SKU
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/catalogs/7c973d2d-e888-4aa6-878d-5b62253cf0ea/remove-skus/',
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
    request.write("{\"sku_uuids\":[\"fcf57d87-19ae-46ad-adea-aad17ccb2d15\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
