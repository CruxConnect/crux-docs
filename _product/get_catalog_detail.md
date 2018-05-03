---
title: /products/catalogs/&lt;catalog_uuid&gt;/
name: Get Catalog Detail
position: 4.01
visibility: public
method: get
description: Get the Details of a particular Catalog you have access to
right_code: |
  ~~~ json
  {
    "uuid": "38504ca3-27ea-4478-85a2-25f01cde1652",
    "supplier": {
      "uuid": "86ab12cd-fd66-4122-8b81-f837bc72d755"
    },
    "skus": [
      {
        "uuid": "bb479ac7-4dd9-4411-a6e9-a265e51aa434"
      },
      {
        "uuid": "95848455-d19b-48f8-8f53-5791818ddeca"
      },
    ],
    "num_skus": 30,
    "default_shipping_cost": null,
    "default_handling_cost": null,
    "retailer": {
      "uuid": "7c8ceed8-86c3-4c4f-9b45-8bda5aa665b2"
    },
    "created": "2018-04-06T01:12:09.804995Z",
    "last_updated": "2018-04-06T01:12:18.259897Z",
    "name": "The industry catalog",
    "description": "Add your description here"
  }
  ~~~
  {: title="Response" }

---
Get the Details of a particular Catalog you have access to.

### URL Parameters:

catalog_uuid
: (string) Universal Unique Identifier for the Catalog

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Catalog

supplier
: (object) The Supplier object contains a supplier_uuid

skus
: (array) An array of SKU objects containing a single sku_uuid objects

num_skus
: (number) The total Number of SKUs per the Catalog

default_shipping_cost
: (number) The Default Shipping Cost parameter contains a Shipping Cost the Supplier determined to be the Default. If null or empty, the Supplier has a variable ship cost per the SKUs or a more sophisticated Shipping strategy.

retailer
: (object) The Retailer object contains a single retailer_uuid.

created
: (string) The Created parameter is the date the Catalog was Created.


last_updated
: (string) The Last Updated parameter is the date the Catalog was Last Updated.

name
: (string) The Name the supplier has designated for this Catalog

description
: (string) The Description the supplier has provided for this Catalog

#### Supplier Object

uuid
: (string) Universal Unique Identifier for the supplier

#### Retailer Object

uuid
: (string) Universal Unique Identifier for the Retailer

#### SKU UUID Object

uuid
: (string) Universal Unique Identifier for the sku

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/products/catalogs/38504ca3-27ea-4478-85a2-25f01cde1652/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/products/catalogs/38504ca3-27ea-4478-85a2-25f01cde1652/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Catalog Detail
    # GET https://api-sandbox.cruxconnect.com/products/catalogs/38504ca3-27ea-4478-85a2-25f01cde1652/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/products/catalogs/38504ca3-27ea-4478-85a2-25f01cde1652/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps()
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
// request Get Catalog Detail
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/catalogs/38504ca3-27ea-4478-85a2-25f01cde1652/',
        method: 'GET',
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
    request.write("{}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
