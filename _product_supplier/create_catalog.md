---
title: /products/catalogs/
name: Create Catalog
position: 2.00
visibility: public
method: post
description: Create a Catalog
right_code: |
  ~~~ json
  {
    "name": "Crux  Worldwide Connection MCdRVj5YLwXkws38oos8grcSHoe45xvU",
    "description": "Crux Worldwide Connection is a test catalog for the purposes of testing"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "7c973d2d-e888-4aa6-878d-5b62253cf0ea",
    "supplier": {
      "uuid": "b5f05054-dce4-4286-96fc-b9424d6b2137"
    },
    "skus": [],
    "num_skus": 0,
    "default_shipping_cost": null,
    "default_handling_cost": null,
    "retailers": [],
    "created": "2018-03-13T20:33:24.960830Z",
    "last_updated": "2018-03-13T20:33:24.960897Z",
    "name": "Crux  Worldwide Connection 0P6bc03TVbnoA73UAP1DrsNnrTpnCDWR",
    "description": "Crux Worldwide Connection is a test catalog for the purposes of testing",
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
: (object) Supplier object containing the supplier uuid

skus
: (array) The SKUs list parameter contains a list of SKU objects containing a single sku_uuid each

num_skus
: (number) The total Number of SKUs per the Catalog

default_shipping_cost
: (number) The Default Shipping Cost parameter contains a Shipping Cost the Supplier determined to be the Default. If null or empty, the Supplier has a variable ship cost per the SKUs or a more sophisticated Shipping strategy.

default_handling_cost
: (number) The Default Handling Cost parameter contains a Handling Cost the Supplier determined to be the Default. If null or empty, the Supplier has a variable handling cost per the SKUs or a more sophisticated handling strategy.

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

# Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/catalogs/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "name": "Crux  Worldwide Connection MCdRVj5YLwXkws38oos8grcSHoe45xvU",
  "description": "Crux Worldwide Connection is a test catalog for the purposes of testing"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/catalogs/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    name="Crux  Worldwide Connection MCdRVj5YLwXkws38oos8grcSHoe45xvU" \
    description="Crux Worldwide Connection is a test catalog for the purposes of testing"

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
            data=json.dumps(    name="Crux  Worldwide Connection MCdRVj5YLwXkws38oos8grcSHoe45xvU" \
    description="Crux Worldwide Connection is a test catalog for the purposes of testing")
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
    request.write("{\"name\":\"Crux  Worldwide Connection MCdRVj5YLwXkws38oos8grcSHoe45xvU\",\"description\":\"Crux Worldwide Connection is a test catalog for the purposes of testing\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
