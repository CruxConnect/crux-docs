---
title: /products/catalogs/
name: Create Catalog
position: 12.00
visibility: public
method: post
description: Create a Catalog
right_code: |
  ~~~ json
  {
    "name": "Crux  Worldwide Connection OtgpdcPYFOlwlN5GM1NPgewoSuIRCQeE",
    "description": "Crux Worldwide Connection is a test catalog for the purposes of testing",
    "default_shipping_cost": "5.33",
    "default_handling_cost": "1.89"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "afdfd2c5-e338-4026-8122-13f5a2373a1a",
    "supplier": {
      "uuid": "7cbf1ff0-3c91-4504-a3cc-c5bedf91f4a9"
    },
    "skus": [],
    "num_skus": 0,
    "default_shipping_cost": 5.33,
    "default_handling_cost": 1.89,
    "retailers": [],
    "created": "2018-04-26T21:21:57.618785Z",
    "last_updated": "2018-04-26T21:21:57.618834Z",
    "name": "Crux  Worldwide Connection 3qBqMnfBdQmQTxIDJV4634FcLd0gei8y",
    "description": "Crux Worldwide Connection is a test catalog for the purposes of testing",
    "is_discoverable": null
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

default_shipping_cost
: (decimal) The Default Shipping Cost parameter contains a Shipping Cost the Supplier determined to be the Default. If null or empty, the Supplier has a variable ship cost per the SKUs or a more sophisticated Shipping strategy. (2 decmial places)

default_handling_cost
: (decimal) The Default Handling Cost parameter contains a Handling Cost the Supplier determined to be the Default. If null or empty, the Supplier has a variable handling cost per the SKUs or a more sophisticated handling strategy. (2 decmial places)

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Catalog

supplier
: (object) Supplier object containing the supplier uuid

skus
: (array) The SKUs list parameter contains a list of SKU objects containing a single sku_uuid each

num_skus
: (integer) The total Number of SKUs per the Catalog

default_shipping_cost
: (decimal) The Default Shipping Cost parameter contains a Shipping Cost the Supplier determined to be the Default. If null or empty, the Supplier has a variable ship cost per the SKUs or a more sophisticated Shipping strategy. (2 decmial places)

default_handling_cost
: (decimal) The Default Handling Cost parameter contains a Handling Cost the Supplier determined to be the Default. If null or empty, the Supplier has a variable handling cost per the SKUs or a more sophisticated handling strategy. (2 decmial places)

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
: (string) The Universal Unique Identifier for the supplier

#### SKUs Object

sku_uuid
: (string) The Universal Unique Identifier for the SKU


#### Retailer Object

retailer_uuid
: (string) The Universal Unique Identifier for the Retailer

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/catalogs/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "default_handling_cost": "1.89",
  "name": "Crux  Worldwide Connection OtgpdcPYFOlwlN5GM1NPgewoSuIRCQeE",
  "description": "Crux Worldwide Connection is a test catalog for the purposes of testing",
  "default_shipping_cost": "5.33"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/catalogs/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    default_handling_cost="1.89" \
    name="Crux  Worldwide Connection OtgpdcPYFOlwlN5GM1NPgewoSuIRCQeE" \
    description="Crux Worldwide Connection is a test catalog for the purposes of testing" \
    default_shipping_cost="5.33"

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
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    default_handling_cost="1.89" \
    name="Crux  Worldwide Connection OtgpdcPYFOlwlN5GM1NPgewoSuIRCQeE" \
    description="Crux Worldwide Connection is a test catalog for the purposes of testing" \
    default_shipping_cost="5.33")
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
    request.write("{\"name\":\"Crux  Worldwide Connection OtgpdcPYFOlwlN5GM1NPgewoSuIRCQeE\",\"description\":\"Crux Worldwide Connection is a test catalog for the purposes of testing\",\"default_shipping_cost\":\"5.33\",\"default_handling_cost\":\"1.89\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
