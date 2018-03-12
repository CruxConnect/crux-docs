---
title: /products/catalogs/
name: Create Catalog
position: 2.02
method: post
description: Create a Catalog
right_code: |
  ~~~ json
  {
    "name": "Spring Thanos Collection P3dI52EbvsjW2LP3htmDVRahafWnEm6v",
    "description": "The Spring Thanos Collection is a test catalog for the purposes of testing"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "9f987473-03e7-46aa-97e8-63d385703ce3",
    "supplier": {
      "uuid": "9ff4ca63-7a46-4eee-a4fb-859e201460c8"
    },
    "skus": [],
    "num_skus": 0,
    "default_shipping_cost": null,
    "retailers": [],
    "created": "2017-11-01T20:12:07.898788Z",
    "last_updated": "2017-11-01T20:12:07.898842Z",
    "name": "Winter Thanos Collection",
    "description": "The Winter Thanos Collection is a test catalog for the purposes of testing",
    "default_shipping_cost_currency": "USD"
  }
  ~~~
  {: title="Response" }

---
Create a new Catalog for Retailers to access.

### Request Parameters:

name
: (string) The Name of the Catalog

description
: (string) The Description for the new Catalog

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Catalog

supplier
: (object) The Supplier object contains a supplier_uuid

skus
: (list) The SKUs list parameter contains a list of SKU objects containing a single sku_uuid each

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

default_shipping_cost_currency
: (string) The Default Shipping Cost Currency parameter indicates what

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
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/catalogs/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "name": "Spring Thanos Collection P3dI52EbvsjW2LP3htmDVRahafWnEm6v",
  "description": "The Spring Thanos Collection is a test catalog for the purposes of testing"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/catalogs/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    name="Spring Thanos Collection P3dI52EbvsjW2LP3htmDVRahafWnEm6v" \
    description="The Spring Thanos Collection is a test catalog for the purposes of testing"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Create Catalog
    # POST https://api-sandbox.cruxconnect.com/products/catalogs/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/catalogs/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    name="Spring Thanos Collection P3dI52EbvsjW2LP3htmDVRahafWnEm6v" \
    description="The Spring Thanos Collection is a test catalog for the purposes of testing")
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
// request Create Catalog
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/catalogs/',
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
    request.write("{\"name\":\"Spring Thanos Collection P3dI52EbvsjW2LP3htmDVRahafWnEm6v\",\"description\":\"The Spring Thanos Collection is a test catalog for the purposes of testing\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
