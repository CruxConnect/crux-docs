---
title: /timp/products/items/
name: Get Items
position: 3.02
visibility: public
method: get
description: Get Items allows you to return a complete list of items you are interested in.
right_code: |
  ~~~ json
  {
    "pagination": {
      "total_count": 150,
      "start": 30,
      "limit": 10,
    },
    "items": [
      {
        "uuid": "5a5fe856-a4bd-4dd2-ac5e-e3c9c29e5ed4",
        "skus": [
          {
            "uuid": "43113405-4964-4086-b5cc-9beea7cb127e",
            "restrictions": null,
            "condition": "new",
            "sku_distinguishing_attributes": {
              "size": 9,
              "color": "azure"
            },
            "sku_nondistinguishing_attributes": {
              "diameter_in_inches": 3.6,
            },
            "minimum_advertised_price": 10,
            "msrp": 113.42,
            "price_tiers": [
              {
                "minimum_tier_quantity": 1,
                "shipping_cost_is_estimate": false,
                "shipping_cost": 1.99,
                "cost": 20.99,
                "catalog": {
                  "name": "The accidental pollution catalog",
                  "uuid": "0692defa-1fbf-4715-b7a2-60690292c37c"
                },
                "shipping_cost_type": "fixed",
                "cost_per_unit": 20.99,
                "handling_cost": 0.99
              },
            ],
            "product_images": [
              {
                "uuid": "49123741-26e0-4f48-9fcf-78f6e84cfdc1",
                "url": "https://picsum.photos/155/?image=15",
                "uri_type": "url",
                "width": 155,
                "height": 155
              },
            ],
            "product_videos": [
              {
                "uuid": "84736294-26e0-4f48-9fcf-78f6e84cfdc1",
                "url": "https://somewhere.videos/155/?video=15",
                "uri_type": "url",
              },
            ],
            "measurements": {
              "sku": {
                "weight_units": null,
                "width": null,
                "dimension_units": null,
                "weight": null,
                "height": null,
                "length": null
              },
              "package": {
                "weight_units": null,
                "width": null,
                "dimension_units": null,
                "weight": null,
                "height": null,
                "length": null
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
                "name": "The absurd ear inventory list"
              },
              {
                "uuid": "5d173491-52ad-4650-91cf-b279475f978d",
                "name": "The ablaze duck inventory list"
              }
            ],
            "created": "2018-04-06T01:12:10.126126Z",
            "last_updated": "2018-04-06T01:12:10.126207Z",
            "sku_id": "bK0bi12ATMo",
            "quantity_in_stock": 19,
            "quantity_on_backorder": 68,
            "number_of_units_bundled": 1,
            "_distinguishing_info_hash": "beACz7hjKsvFEnTGWQBuJ6",
            "minimum_advertised_price_currency": "USD",
            "msrp_currency": "USD",
            "item": {
              "uuid": "5a5fe856-a4bd-4dd2-ac5e-e3c9c29e5ed4"
            },
            "_sku_measurements": null,
            "_package_measurements": null
          }
        ],
        "restrict_from_marketplaces": [],
        "supplier": {
          "uuid": "86ab12cd-fd66-4122-8b81-f837bc72d755",
          "name": "Morales, Martin and Bautista"
        },
        "cost_range": {
          "max": 100.12,
          "min": 17.76
        },
        "minimum_advertised_price_range": {
          "max": 10,
          "min": 10
        },
        "msrp_range": {
          "max": 159.7,
          "min": 54.08
        },
        "product_images": [
          {
            "uuid": "8103e697-6a17-4dd1-939b-3d7ca9676b1c",
            "url": "https://picsum.photos/155/?image=10",
            "width": 155,
            "height": 155
          },
        ],
        "product_videos": [
          {
            "uuid": "846284309-26e0-4f48-9fcf-78f6e84cfdc1",
            "url": "https://somewhere.videos/155/?video=15",
            "width": 155,
            "height": 155
          },
        ],
        "categories": [
          {
            "uuid": "266a9a41-58a0-429e-8275-791f169789d1",
            "path": [
              "candid mouth l0",
              "inexpensive mouth l1"
            ],
            "description": ""
          }
        ],
        "created": "2018-04-06T01:12:10.001127Z",
        "last_updated": "2018-04-06T01:12:10.001188Z",
        "item_id": "7FZvMyg0BjfewNJJ",
        "title": "The insistent room item",
        "description": "Underneath all that able rest there will be insistent room item. Watching. Waiting. Wanting. Wishing. Wondering. Even in abashed sunlight our insistent room item works like a rest!It will blow your abashed mind.Then tacos will start raining right out of the abashed sky.Because it's the best insistent room item a person get possibly get.  At least on a abashed Tuesday! When it's all said and done, there's still insistent room item. Still. You know you want it. Because we care about how your insistent room item looks!",
        "warranty": "A inborn warranty",
        "return_policy": null,
        "manufacturer": "direction Corp.",
        "brand": "orange brand",
        "country_of_origin": "CX",
        "shipping_origin_country": "TZ",
        "other_marketplace_restriction": null,
        "fba_certified": null,
        "item_attributes": {
          "hardness": 12,
          "hair-color": "brown"
        }
      },
    ]
  }
  ~~~
  {: title="Response" }

---
Get Item List allows you to return a complete list of items you are interested in.

### Response Parameters:

An array of item objects is returned

#### Item Object

{% include timp/product/response/item.md %}

#### SKU Object:

{% include timp/product/response/sku.md %}

#### Price Tier Object:

{% include timp/product/response/price_tier.md %}

#### Product Image Object:

{% include timp/product/response/image.md %}

#### Product Videos Object:

{% include timp/product/response/video.md %}

#### SKU Measurements Object:

{% include timp/product/response/measurements_sku.md %}

#### Package Measurements Object:

{% include timp/product/response/measurements_package.md %}

#### Product Identifiers Object:

{% include timp/product/response/product_identifiers.md %}

#### Inventory List Object:

{% include timp/product/response/inventory_list_minimal.md %}

#### Supplier Object:

{% include timp/product/response/supplier_minimal.md %}

#### Cost Range Object:

{% include timp/product/response/cost_range.md %}

#### Minimum Advertized Price Range Object:

{% include timp/product/response/map_range.md %}

#### Manufacturer's Suggested Retail Price (MSRP) Range Object:

{% include timp/product/response/msrp_range.md %}

#### Item Product Images Object:

{% include timp/product/response/image.md %}

#### Item Product Videos Object:

{% include timp/product/response/video.md %}

# Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/timp/products/items/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/timp/products/items/' \
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
    # Get Items
    # GET https://api-sandbox.cruxconnect.com/timp/products/items/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/timp/products/items/",
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
// request Get Items
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/products/items/',
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
