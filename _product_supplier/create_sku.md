---
title: /timp/products/skus/
name: Create SKU
position: 11.07
visibility: public
method: post
description: Create a SKU to add to a specified item_uuid
right_code: |
  ~~~ json
  {
    "item": {
      "uuid": "905c3e4b-ef10-4f77-b07e-03d4ecb743a0"
    },
    "sku_id": "Lvfnsf-jwoQ0qLQ-H3tUmrVi",
    "restrictions": "tmpunavail",
    "condition": "used",
    "quantity_in_stock": "500",
    "quantity_on_backorder": "100",
    "number_of_units_bundled": "2",
    "distinguishing_attributes": {
      "color": "blue"
    },
    "minimum_advertised_price": "40.00",
    "msrp": "55.99",
    "minimum_advertised_price_currency": "USD",
    "msrp_currency": "USD"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "4c443958-eb6f-4043-8cbc-b227e044334e",
    "restrictions": "tmpunavail",
    "condition": "used",
    "sku_distinguishing_attributes": {},
    "item": {
      "uuid": "905c3e4b-ef10-4f77-b07e-03d4ecb743a0"
    },
    "minimum_advertised_price": 40,
    "msrp": 55.99,
    "price_tiers": [],
    "product_images": [],
    "product_videos": [],
    "measurements": {
      "sku": {
        "weight": null,
        "weight_units": null,
        "length": null,
        "width": null,
        "height": null,
        "dimension_units": null
      },
      "package": {
        "weight": null,
        "weight_units": null,
        "length": null,
        "width": null,
        "height": null,
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
    "catalogs": [
      {
        "uuid": "96ce2c9d-044f-4208-9148-5e4b5b2771cb",
        "name": "__master__"
      }
    ],
    "created": "2018-08-24T22:45:10.623218Z",
    "last_updated": "2018-08-24T22:45:10.623271Z",
    "sku_id": "AKpvhb-UhLREqWn-cO3bLy4P",
    "quantity_in_stock": 500,
    "quantity_on_backorder": 100,
    "number_of_units_bundled": 2,
    "sku_nondistinguishing_attributes": {}
  }
  ~~~
  {: title="Response" }

---
Create a SKU to add to a specified item_uuid.

### Request Parameters:

{% include timp/product/request/sku.md %}

### Request Parameters:

{% include timp/product/request/sku.md %}

### Response Parameters:

{% include timp/product/response/sku.md %}

#### SKU Distinguishing Attributes Object:

{% include timp/objects/attributes.md %}

#### Price Tier Object:

{% include timp/objects/price_tier.md %}

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

#### Catalog Object:

{% include timp/product/response/catalog_simple.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}

### Expected Response Codes

# Short Description
Create a SKU to add to a specified item_uuid

# Long Description
Create a SKU to add to a specified item_uuid.

### Request Parameters:

{% include timp/product/request/sku.md %}

### Request Parameters:

{% include timp/product/request/sku.md %}

### Response Parameters:

{% include timp/product/response/sku.md %}

#### SKU Distinguishing Attributes Object:

{% include timp/objects/attributes.md %}

#### Price Tier Object:

{% include timp/objects/price_tier.md %}

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

#### Catalog Object:

{% include timp/product/response/catalog_simple.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/timp/products/skus/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "restrictions": "tmpunavail",
  "number_of_units_bundled": "2",
  "condition": "used",
  "minimum_advertised_price_currency": "USD",
  "item": {
    "uuid": "905c3e4b-ef10-4f77-b07e-03d4ecb743a0"
  },
  "sku_id": "Lvfnsf-jwoQ0qLQ-H3tUmrVi",
  "msrp": "55.99",
  "quantity_in_stock": "500",
  "minimum_advertised_price": "40.00",
  "msrp_currency": "USD",
  "quantity_on_backorder": "100",
  "distinguishing_attributes": {
    "color": "blue"
  }
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/timp/products/skus/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    restrictions="tmpunavail" \
    number_of_units_bundled="2" \
    condition="used" \
    minimum_advertised_price_currency="USD" \
    item:="{
  \"uuid\": \"905c3e4b-ef10-4f77-b07e-03d4ecb743a0\"
}" \
    sku_id="Lvfnsf-jwoQ0qLQ-H3tUmrVi" \
    msrp="55.99" \
    quantity_in_stock="500" \
    minimum_advertised_price="40.00" \
    msrp_currency="USD" \
    quantity_on_backorder="100" \
    distinguishing_attributes:="{
  \"color\": \"blue\"
}"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Create SKU
    # POST https://api-sandbox.cruxconnect.com/timp/products/skus/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/timp/products/skus/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    restrictions="tmpunavail" \
    number_of_units_bundled="2" \
    condition="used" \
    minimum_advertised_price_currency="USD" \
    item:="{
  \"uuid\": \"905c3e4b-ef10-4f77-b07e-03d4ecb743a0\"
}" \
    sku_id="Lvfnsf-jwoQ0qLQ-H3tUmrVi" \
    msrp="55.99" \
    quantity_in_stock="500" \
    minimum_advertised_price="40.00" \
    msrp_currency="USD" \
    quantity_on_backorder="100" \
    distinguishing_attributes:="{
  \"color\": \"blue\"
}")
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
// request Create SKU
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/products/skus/',
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
    request.write("{\"item\":{\"uuid\":\"905c3e4b-ef10-4f77-b07e-03d4ecb743a0\"},\"sku_id\":\"Lvfnsf-jwoQ0qLQ-H3tUmrVi\",\"restrictions\":\"tmpunavail\",\"condition\":\"used\",\"quantity_in_stock\":\"500\",\"quantity_on_backorder\":\"100\",\"number_of_units_bundled\":\"2\",\"distinguishing_attributes\":{\"color\":\"blue\"},\"minimum_advertised_price\":\"40.00\",\"msrp\":\"55.99\",\"minimum_advertised_price_currency\":\"USD\",\"msrp_currency\":\"USD\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
