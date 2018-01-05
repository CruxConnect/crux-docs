---
title: /api/products/skus/search/completion/
name: SKU Autocomplete - Retailer
position: 2.27
method: post
description: SKU Autocomplete allows you to search for a SKU without having the complete sku_id or sku_uuid
right_code: |
  ~~~ json
  {
    "partial": "Z"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "skus": [
      {
        "uuid": "66f8b469-f702-4e4f-89ec-b7131a5225f1",
        "sku_id": "5Z0CurC5",
        "number_of_units_bundled": 4,
        "price_tiers": [
          {
            "shipping_cost": 1.99,
            "shipping_cost_is_estimate": true,
            "minimum_tier_quantity": 2,
            "cost": 100.12
          },
          {
            "shipping_cost": 0.99,
            "shipping_cost_is_estimate": true,
            "minimum_tier_quantity": 4,
            "cost": 75.6
          },
          {
            "shipping_cost": 0,
            "shipping_cost_is_estimate": true,
            "minimum_tier_quantity": 16,
            "cost": 49.99
          }
        ],
        "product_images": [
          {
            "uuid": "7800e2e6-6748-40f1-9a4d-cb6880ea0538",
            "url": "https://api.adorable.io/avatars/155/obad15.png",
            "height": 155,
            "width": 155
          },
          {
            "uuid": "e8736e75-a021-414f-bbfe-146db16b8e08",
            "url": "https://api.adorable.io/avatars/285/obad15.png",
            "height": 285,
            "width": 285
          }
        ],
        "org_uuids": [
          "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
          "5e85605d-b2e8-4f10-9ecb-675190118065",
          "2d3845d0-4325-44b0-a505-c8c68227380e"
        ]
      },
      {
        "uuid": "abbe37bf-c5ba-4080-b048-cd9cc1f72e5c",
        "sku_id": "ZcMp0Hkml81kkJnH",
        "number_of_units_bundled": 1,
        "price_tiers": [
          {
            "shipping_cost": 1.99,
            "shipping_cost_is_estimate": false,
            "minimum_tier_quantity": 1,
            "cost": 20.99
          },
          {
            "shipping_cost": 0.99,
            "shipping_cost_is_estimate": false,
            "minimum_tier_quantity": 12,
            "cost": 18.12
          },
          {
            "shipping_cost": 0,
            "shipping_cost_is_estimate": false,
            "minimum_tier_quantity": 100,
            "cost": 17.76
          }
        ],
        "product_images": [
          {
            "uuid": "473e164b-55a5-4520-be4b-c2223ec9361b",
            "url": "https://api.adorable.io/avatars/285/obad33.png",
            "height": 285,
            "width": 285
          },
          {
            "uuid": "6da1fe0b-d052-4590-b946-b28c5cecd28a",
            "url": "https://api.adorable.io/avatars/155/obad39.png",
            "height": 155,
            "width": 155
          }
        ],
        "org_uuids": [
          "0e9dd1c1-1eb5-45dc-9bb0-fe3d53f9da0d",
          "a070146b-409c-4a36-8bc4-565881a71bea"
        ]
      }
    ]
  }
  ~~~
  {: title="Response" }

---
SKU Autocomplete allows you to search for a SKU without having the complete sku_id or sku_uuid. You can provide a partial sku_id or sku_uuid and you receive a list of results that are close if not an exact match for the SKU you're searching for.

### Response Parameters:

skus
: (list) The SKUs list parameter contains the list of SKU objects that match the partial sku_id or sku_uuid you provided

#### SKU Object:

org_uuids
: (list) The Univeral Unique Identifiers for the Organization list parameter contains the list of org_uuids that may access this SKU

product_images
: (list) The Product Images list parameter contains the SKU Product Image objects

sku_id
: (string) The Stock Keeping Unit (SKU) Identifier for the SKU as provided by the Supplier

uuid
: (string) The Universal Unique Identifier for the SKU

number_of_units_bundled
: (number) The Number of Units Bundled parameter indicates how many SKUs are in a single bundle.

price_tiers
: (list) The list of Price Tier objects on this SKU including shipping_cost, minimum_tier_quantity, cost, shipping_cost_is_estimate.

#### Product Image Object:

uuid
: (string) The Universal Unique Identifier for the SKU Product Image

url
: (string) The URL for the SKU Product Image

width
: (number) The Image Width in pixels for the SKU Product Image

height
: (number) The Image Height in pixels for the SKU Product Image

#### Price Tier Object:

shipping_cost
: (number) The Shipping Cost per the SKU per the Price Tier

minimum_tier_quantity
: (number) The Minimum Tier Quantity per the SKU per the Price Tier

cost
: (number) The Cost per the SKU per the Price Tier

shipping_cost_is_estimate
: (boolean) The Shipping Cost is Estimate parameter answers the question whether the shipping cost is an estimate per the SKU per the Price Tier.

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
curl -X "POST" "https://stable.projectthanos.com/api/products/skus/search/completion/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "partial": "Z"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://stable.projectthanos.com/api/products/skus/search/completion/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8' \
    partial="Z"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # SKU Autocomplete - Retailer
    # POST https://stable.projectthanos.com/api/products/skus/search/completion/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/products/skus/search/completion/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    partial="Z")
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
// request SKU Autocomplete - Retailer
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/products/skus/search/completion/',
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
    request.write("{\"partial\":\"Z\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
