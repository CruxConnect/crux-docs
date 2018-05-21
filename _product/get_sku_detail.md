---
title: /products/skus/&ltsku_uuid&gt/
name: Get Sku Detail
position: 4.08
visibility: public
method: get
description: Get Details about a SKU
right_code: |
  ~~~ json
  {
    "skus": [
      {
        "quantity": "72",
        "sku_id": "WONKYWILLA1"
      },
    ],
    "po_number": "po-PSJrQDYh",
    "notes": "here are some notes",
    "shipping_carrier": "UPS",
    "shipping_method": "Ground",
    "address": {
      "name": "Bob Iger",
      "business_name": "NBC",
      "address1": "30 Rockefeller Plaza",
      "address2": "STE 123",
      "city": "New York",
      "state": "NY",
      "postal_code": "10112"
    }
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "95848455-d19b-48f8-8f53-5791818ddeca",
    "restrictions": null,
    "condition": "refurb",
    "distinguishing_attributes": {
      "size": 9,
      "color": "antiquewhite"
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
        "cost": 20.99,
        "cost_per_unit": 0.9995238095238095,
        "shipping_cost": 1.99,
        "minimum_tier_quantity": 1
      },
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
        "uuid": "84730687-b160-4dea-9740-3eaa98886ccd",
        "url": "https://somewhere.videos/285/?video=32",
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
        "name": "The absurd ear inventory list"
      },
      {
        "uuid": "5d173491-52ad-4650-91cf-b279475f978d",
        "name": "The ablaze duck inventory list"
      }
    ],
    "created": "2018-04-06T01:12:10.036088Z",
    "last_updated": "2018-04-06T01:12:10.036182Z",
    "sku_id": "wQWFpGc",
    "quantity_in_stock": null,
    "quantity_on_backorder": 79,
    "number_of_units_bundled": 21
  }
  ~~~
  {: title="Response" }

---
Get Details about a SKU. There is a varying amount of data provided with each SKUs. The Response Parameters listed below are potential attributes of SKUs that may be returned to you.

### URL Parameters:

sku_uuid
: (string) The Universal Unique Identifier for the SKU

### Response Parameters:

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
curl "https://api-sandbox.cruxconnect.com/products/skus/95848455-d19b-48f8-8f53-5791818ddeca/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "address": {
    "state": "NY",
    "city": "New York",
    "address1": "30 Rockefeller Plaza",
    "business_name": "NBC",
    "postal_code": "10112",
    "name": "Bob Iger",
    "address2": "STE 123"
  },
  "shipping_carrier": "UPS",
  "po_number": "po-PSJrQDYh",
  "notes": "here are some notes",
  "skus": [
    {
      "quantity": "72",
      "sku_id": "WONKYWILLA1"
    },
    {
      "quantity": "848",
      "sku_id": "CHOCO77"
    }
  ],
  "shipping_method": "Ground"
}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/products/skus/95848455-d19b-48f8-8f53-5791818ddeca/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    address:="{
  \"state\": \"NY\",
  \"city\": \"New York\",
  \"address1\": \"30 Rockefeller Plaza\",
  \"business_name\": \"NBC\",
  \"postal_code\": \"10112\",
  \"name\": \"Bob Iger\",
  \"address2\": \"STE 123\"
}" \
    shipping_carrier="UPS" \
    po_number="po-PSJrQDYh" \
    notes="here are some notes" \
    skus:="[
  {
    \"quantity\": \"72\",
    \"sku_id\": \"WONKYWILLA1\"
  },
  {
    \"quantity\": \"848\",
    \"sku_id\": \"CHOCO77\"
  }
]" \
    shipping_method="Ground"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Sku Detail
    # GET https://api-sandbox.cruxconnect.com/products/skus/95848455-d19b-48f8-8f53-5791818ddeca/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/products/skus/95848455-d19b-48f8-8f53-5791818ddeca/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    address:="{
  \"state\": \"NY\",
  \"city\": \"New York\",
  \"address1\": \"30 Rockefeller Plaza\",
  \"business_name\": \"NBC\",
  \"postal_code\": \"10112\",
  \"name\": \"Bob Iger\",
  \"address2\": \"STE 123\"
}" \
    shipping_carrier="UPS" \
    po_number="po-PSJrQDYh" \
    notes="here are some notes" \
    skus:="[
  {
    \"quantity\": \"72\",
    \"sku_id\": \"WONKYWILLA1\"
  },
  {
    \"quantity\": \"848\",
    \"sku_id\": \"CHOCO77\"
  }
]" \
    shipping_method="Ground")
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
// request Get Sku Detail
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/skus/95848455-d19b-48f8-8f53-5791818ddeca/',
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
    request.write("{\"skus\":[{\"quantity\":\"72\",\"sku_id\":\"WONKYWILLA1\"},{\"quantity\":\"848\",\"sku_id\":\"CHOCO77\"}],\"po_number\":\"po-PSJrQDYh\",\"notes\":\"here are some notes\",\"shipping_carrier\":\"UPS\",\"shipping_method\":\"Ground\",\"address\":{\"name\":\"Bob Iger\",\"business_name\":\"NBC\",\"address1\":\"30 Rockefeller Plaza\",\"address2\":\"STE 123\",\"city\":\"New York\",\"state\":\"NY\",\"postal_code\":\"10112\"}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
