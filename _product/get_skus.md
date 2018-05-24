---
title: /products/skus/
name: Get SKUs
position: 4.07
visibility: public
method: get
description: Get SKUs allows you to return a complete list of SKUs you are interested in.
right_code: |
  ~~~ json
  [
    {
      "uuid": "95848455-d19b-48f8-8f53-5791818ddeca",
      "restrictions": null,
      "condition": "refurb",
      "sku_distinguishing_attributes": {
        "size": 9,
        "color": "antiquewhite"
      },
      "sku_nondistinguishing_attributes": {
        "diameter_in_inches": 3.6,
      },
      "item": {
        "uuid": "5a5fe856-a4bd-4dd2-ac5e-e3c9c29e5ed4"
      },
      "minimum_advertised_price": 10,
      "msrp": 54.08,
      "price_tiers": [
        {
          "handling_cost": 0.99,
          "shipping_cost_type": "fixed",
          "catalog": {
            "name": "The accidental pollution catalog",
            "uuid": "0692defa-1fbf-4715-b7a2-60690292c37c"
          },
          "shipping_cost_is_estimate": false,
          "cost": 18.12,
          "cost_per_unit": 0.8628571428571429,
          "shipping_cost": 0.99,
          "minimum_tier_quantity": 12
        }
      ],
      "product_images": [
        {
          "uuid": "97fa6aad-b160-4dea-9740-3eaa98886ccd",
          "url": "https://picsum.photos/285/?image=17",
          "uri_type": "url",
          "width": 285,
          "height": 285
        },
      ],
      "product_videos": [
        {
          "uuid": "94726495-b160-4dea-9740-3eaa98886ccd",
          "url": "https://somewhere.videos/285/?video=17",
          "uri_type": "url",
        },
      ],
      "measurements": {
        "package": {
          "height": null,
          "length": null,
          "width": null,
          "weight_units": null,
          "weight": null,
          "dimension_units": null
        },
        "sku": {
          "height": null,
          "length": null,
          "width": null,
          "weight_units": null,
          "weight": null,
          "dimension_units": null
        }
      },
      "product_identifiers": {
        "upca": null,
        "ean13": null,
        "gtin14": null,
        "isbn": null,
        "asin": null,
        "mpn": null
      },
      "inventory_lists": [
        {
          "uuid": "1431483d-f893-45a4-8a73-0a46c44d15c5",
          "name": "The absurd ear Inventory List"
        },
        {
          "uuid": "5d173491-52ad-4650-91cf-b279475f978d",
          "name": "The ablaze duck Inventory List"
        }
      ],
      "created": "2018-04-06T01:12:10.036088Z",
      "last_updated": "2018-04-06T01:12:10.036182Z",
      "sku_id": "wQWFpGc",
      "quantity_in_stock": null,
      "quantity_on_backorder": 79,
      "number_of_units_bundled": 21
    }
  ]
  ~~~
  {: title="Response" }

---
Return a complete list of SKUs

### Response Parameters:

An array of SKU Objects

#### SKU Object

{% include product/response/sku.md %}

#### Price Tier Object:

{% include product/response/price_tier.md %}

#### Product Image Object:

{% include product/response/image.md %}

#### Product Video Object:

{% include product/response/video.md %}

#### SKU Measurements Object:

{% include product/response/measurements_sku.md %}

#### Package Measurements Object:

{% include product/response/measurements_package.md %}

#### Product Identifiers Object:

{% include product/response/product_identifiers.md %}

#### Inventory List Object:

{% include product/response/inventory_list_minimal.md %}

#### Supplier Object:

{% include product/response/supplier_minimal.md %}

### Expected Response Codes

{% include links/response_codes.md %}

~~~ bash
curl "https://api-sandbox.cruxconnect.com/products/skus/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/products/skus/' \
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
    # Get SKUs
    # GET https://api-sandbox.cruxconnect.com/products/skus/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/products/skus/",
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
// request Get SKUs
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/skus/',
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
