---
title: /api/products/skus/search/completion/
name: SKU Autocomplete - Retailer
position: 2.27
type: post
description: SKU Autocomplete allows you to search for a SKU without having the complete sku_id or sku_uuid
right_code: |
  ~~~ json
  {
    "partial": "A"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "skus": [
      {
        "sku_id": "A6yIzsn83j921",
        "owner_uuid": "1bd645dd-f2d8-401b-aa79-cfb990851fe9",
        "distinguishing_info": {
          "number_of_units_bundled": 1000,
          "distinguishing_attributes": {
            "apparel-size": "XXXXS",
            "color": "blue"
          },
          "condition": "used"
        },
        "price_tiers": [
          {
            "minimum_tier_quantity": 2,
            "shipping_cost": 1.99,
            "cost": 100.12,
            "shipping_cost_is_estimate": true
          },
          {
            "minimum_tier_quantity": 4,
            "shipping_cost": 0.99,
            "cost": 75.6,
            "shipping_cost_is_estimate": true
          },
          {
            "minimum_tier_quantity": 16,
            "shipping_cost": 0,
            "cost": 49.99,
            "shipping_cost_is_estimate": true
          }
        ],
        "item_title": "The inborn color item",
        "uuid": "6e804cc7-3e5f-44dc-a02e-7eb0adc4ee39",
        "supplier_uuid": "cb8677c0-9e3e-4ec9-9b01-4662578a6736",
        "product_images": [
          {
            "width": 80,
            "uuid": "df82601f-90b1-4fde-8311-54ddb5873bfb",
            "url": "https://api.adorable.io/avatars/80/obad30.png",
            "height": 80
          },
          {
            "width": 155,
            "uuid": "feb6e877-4d9f-41ac-a009-9635e7e6ea77",
            "url": "https://api.adorable.io/avatars/155/obad39.png",
            "height": 155
          }
        ]
      },
      {
        "sku_id": "aVCos8HBAf2H",
        "owner_uuid": "1bd645dd-f2d8-401b-aa79-cfb990851fe9",
        "distinguishing_info": {
          "number_of_units_bundled": 12,
          "distinguishing_attributes": {
            "apparel-size": "XXXXS"
          },
          "condition": "used"
        },
        "price_tiers": [
          {
            "minimum_tier_quantity": 2,
            "shipping_cost": 1.99,
            "cost": 100.12,
            "shipping_cost_is_estimate": true
          },
          {
            "minimum_tier_quantity": 4,
            "shipping_cost": 0.99,
            "cost": 75.6,
            "shipping_cost_is_estimate": true
          },
          {
            "minimum_tier_quantity": 16,
            "shipping_cost": 0,
            "cost": 49.99,
            "shipping_cost_is_estimate": true
          }
        ],
        "item_title": "The elfin year item",
        "uuid": "ac452a39-bd06-4be2-91e4-d9b0fa9fab36",
        "supplier_uuid": "21e16bf4-312f-4352-8569-9be60894473a",
        "product_images": [
          {
            "width": 155,
            "uuid": "ceccb86d-0820-48ee-ab85-4fdad7dde447",
            "url": "https://api.adorable.io/avatars/155/obad39.png",
            "height": 155
          },
          {
            "width": 80,
            "uuid": "d1be61ed-0d80-4953-b168-fe054584dff2",
            "url": "https://api.adorable.io/avatars/80/obad33.png",
            "height": 80
          }
        ]
      }
    ]
  }
  ~~~
  {: title="Response" }

---
SKU Autocomplete allows you to search for a SKU without having the complete sku_id or sku_uuid. You can provide a partial sku_id or sku_uuid and you receive a list of results that are close if not an exact match for the SKU you're searching for.

URL Endpoint: /api/products/skus/search/completion/

### Response Parameters:

skus
: (list) The SKUs list parameter contains the list of SKU objects that match the partial sku_id you provided

#### SKU Object:

sku_id
: (string) The Stock Keeping Unit (SKU) Identifier for the SKU as provided by the Supplier

owner_uuids
: (list) The Univeral Unique Identifiers for the Owner of the sku_id

distinguishing_info
(object) Information that distinguishes this SKU from others belonging to the same item. (e.g. condition, # of units bundled, size, etc.)

price_tiers
: (list) The list of Price Tier objects on this SKU including shipping_cost, minimum_tier_quantity, cost, shipping_cost_is_estimate.

item_title
: (string) The Title for the Item

uuid
: (string) The Universal Unique Identifier for the SKU

supplier_uuid
: (string) The Unviersal Unique Identifier for the Supplier

product_images
: (list) The Product Images list parameter contains urls and dimensions for each image

#### Distinguishing Info Object:

number_of_units_bundled
: (number) The Number of Units Bundled parameter indicates the quantity included in a bundle

distinguishing_attributes
: (object) The Distinguishing Attributes are attributes which based on a category or product line may be necessary to include. It may also be empty, as per the Suppliers' discretion.

condition
: (string) The Condition of the SKU (e.g. "new", "used", "refurbished", etc.)

#### Price Tier Object:

shipping_cost
: (number) The Shipping Cost per the SKU per the Price Tier

minimum_tier_quantity
: (number) The Minimum Tier Quantity per the SKU per the Price Tier

cost
: (number) The Cost per the SKU per the Price Tier

shipping_cost_is_estimate
: (boolean) The Shipping Cost is Estimate parameter answers the question whether the shipping cost is an estimate per the SKU per the Price Tier.

#### Product Image Object:

uuid
: (string) The Universal Unique Identifier for the SKU Product Image

url
: (string) The URL for the SKU Product Image

width
: (number) The Image Width in pixels for the SKU Product Image

height
: (number) The Image Height in pixels for the SKU Product Image

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
     -H 'Authorization: Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "partial": "A"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://stable.projectthanos.com/api/products/skus/search/completion/' \
    'Authorization':'Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c' \
    'Content-Type':'application/json; charset=utf-8' \
    partial="A"

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
                "Authorization": "Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    partial="A")
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
        headers: {"Authorization":"Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"partial\":\"A\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }

