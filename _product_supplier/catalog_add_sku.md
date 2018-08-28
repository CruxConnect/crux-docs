---
title: /timp/products/catalogs/&lt;catalog_uuid&gt;/add-skus/
name: Catalog Add SKU
position: 11.06
visibility: public
method: post
description: Add already existing SKUs to a Catalog
right_code: |
  ~~~ json
  {
    "sku_uuids": [
      ""
    ]
  }
  ~~~
  {: title="Request" }

  ~~~ json
  null
  ~~~
  {: title="Response" }

---
Add already existing SKUs to a Catalog for Retailers to access. By providing your catalog_uuid in the URL and array of sku_uuids, you can successfully add them to items previously included in the indicated Catalog.

### URL Parameters

catalog_uuid
: (string) Universal Unique Identifier for the catalog to which the sku will be added

### Request Parameters:

sku_uuids
: (array) The SKU UUIDs parameter holds an array of sku_uuids

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/timp/products/catalogs/f3603476-1f48-4ef9-a76c-0ec2f9c612fc/add-skus/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "sku_uuids": [
    ""
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/timp/products/catalogs/f3603476-1f48-4ef9-a76c-0ec2f9c612fc/add-skus/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    sku_uuids:="[
  \"\"
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
    # POST https://api-sandbox.cruxconnect.com/timp/products/catalogs/f3603476-1f48-4ef9-a76c-0ec2f9c612fc/add-skus/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/timp/products/catalogs/f3603476-1f48-4ef9-a76c-0ec2f9c612fc/add-skus/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    sku_uuids:="[
  \"\"
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
        path: '/timp/products/catalogs/f3603476-1f48-4ef9-a76c-0ec2f9c612fc/add-skus/',
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
    request.write("{\"sku_uuids\":[\"\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
