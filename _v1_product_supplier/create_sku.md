---
title: /products/skus/
name: Create SKU
position: 12.07
visibility: v1
method: post
description: Create a SKU to add to a specified item_uuid
right_code: |
  ~~~ json
  {
    "item": {
      "uuid": "c278fcc7-ff5e-4494-9ccf-36d6d6d167c8"
    },
    "sku_id": "LYsNxu-iIhTgvti-X3qj0ade",
    "restrictions": "tmpunavail",
    "condition": "used",
    "quantity_in_stock": "500",
    "quantity_on_backorder": "100",
    "number_of_units_bundled": "2",
    "sku_distinguishing_attributes": {
      "color": "blue"
    },
    "sku_nondistinguishing_attributes": {
      "diameter_in_inches": 3.4,
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
    "uuid": "7be0e3de-4108-4b08-85b4-19ddd0adcae4",
    "restrictions": "tmpunavail",
    "condition": "used",
    "sku_distinguishing_attributes": {
      "color": "blue"
    },
    "sku_nondistinguishing_attributes": {
      "diameter_in_inches": 3.4,
    },
    "item": {
      "uuid": "2bce11c2-e60c-47a0-899b-81edfa90f666"
    },
    "minimum_advertised_price": 40,
    "msrp": 55.99,
    "price_tiers": [],
    "product_images": [],
    "product_videos": [],
    "measurements": {
      "sku": {
        "weight_units": null,
        "weight": null,
        "height": null,
        "width": null,
        "dimension_units": null,
        "length": null
      },
      "package": {
        "weight_units": null,
        "weight": null,
        "height": null,
        "width": null,
        "dimension_units": null,
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
    "catalogs": [
      {
        "uuid": "81bd100e-e347-4ee3-9dfd-79a7a59aaa72",
        "name": "__master__"
      }
    ],
    "created": "2018-04-25T22:24:27.631175Z",
    "last_updated": "2018-04-25T22:24:27.631223Z",
    "sku_id": "DtMEqi-mWpAhAe5-qLuMx5Rc",
    "quantity_in_stock": 500,
    "quantity_on_backorder": 100,
    "number_of_units_bundled": 2
  }
  ~~~
  {: title="Response" }

---
Create a SKU to add to a specified item_uuid.

### Request Parameters:

{% include v1/product/request/sku.md %}

### Response Parameters:

{% include v1/product/response/sku.md %}

#### SKU Distinguishing Attributes Object:

{% include v1/objects/attributes.md %}

#### Price Tier Object:

{% include v1/objects/price_tier.md %}

#### Product Image Object:

{% include v1/product/response/image.md %}

#### Product Videos Object:

{% include v1/product/response/video.md %}

#### SKU Measurements Object:

{% include v1/product/response/measurements_sku.md %}

#### Package Measurements Object:

{% include v1/product/response/measurements_package.md %}

#### Product Identifiers Object:

{% include v1/product/response/product_identifiers.md %}

#### Catalog Object:

{% include v1/product/response/catalog_simple.md %}

### Expected Response Codes

{% include v1/links/response_codes.md %}

~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/skus/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "restrictions": "tmpunavail",
  "number_of_units_bundled": "2",
  "condition": "used",
  "minimum_advertised_price_currency": "USD",
  "item": {
    "uuid": "c278fcc7-ff5e-4494-9ccf-36d6d6d167c8"
  },
  "sku_id": "LYsNxu-iIhTgvti-X3qj0ade",
  "msrp": "55.99",
  "quantity_in_stock": "500",
  "minimum_advertised_price": "40.00",
  "msrp_currency": "USD",
  "quantity_on_backorder": "100",
  "sku_distinguishing_attributes": {
    "color": "blue"
  },
  "sku_nondistinguishing_attributes": {
    "diameter_in_inches": 3.4,
  },
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/skus/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    restrictions="tmpunavail" \
    number_of_units_bundled="2" \
    condition="used" \
    minimum_advertised_price_currency="USD" \
    item:="{
  \"uuid\": \"c278fcc7-ff5e-4494-9ccf-36d6d6d167c8\"
}" \
    sku_id="LYsNxu-iIhTgvti-X3qj0ade" \
    msrp="55.99" \
    quantity_in_stock="500" \
    minimum_advertised_price="40.00" \
    msrp_currency="USD" \
    quantity_on_backorder="100" \
    sku_distinguishing_attributes:="{
  \"color\": \"blue\"
}"
    sku_nondistinguishing_attributes:="{
  \"diameter_in_inches\": \"3.5\"
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
    # POST https://api-sandbox.cruxconnect.com/products/skus/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/skus/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    restrictions="tmpunavail" \
    number_of_units_bundled="2" \
    condition="used" \
    minimum_advertised_price_currency="USD" \
    item:="{
  \"uuid\": \"c278fcc7-ff5e-4494-9ccf-36d6d6d167c8\"
}" \
    sku_id="LYsNxu-iIhTgvti-X3qj0ade" \
    msrp="55.99" \
    quantity_in_stock="500" \
    minimum_advertised_price="40.00" \
    msrp_currency="USD" \
    quantity_on_backorder="100" \
    sku_nondistinguishing_attributes:="{
  \"diameter_in_inches\": \"3.5\"
}" \
    sku_distinguishing_attributes:="{
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
        path: '/products/skus/',
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
    request.write("{\"item\":{\"uuid\":\"c278fcc7-ff5e-4494-9ccf-36d6d6d167c8\"},\"sku_id\":\"LYsNxu-iIhTgvti-X3qj0ade\",\"restrictions\":\"tmpunavail\",\"condition\":\"used\",\"quantity_in_stock\":\"500\",\"quantity_on_backorder\":\"100\",\"number_of_units_bundled\":\"2\",\"sku_distinguishing_attributes\":{\"color\":\"blue\"},\"sku_nondistinguishing_attributes\":{\"diameter_in_inches\":\"3.5\"},\"minimum_advertised_price\":\"40.00\",\"msrp\":\"55.99\",\"minimum_advertised_price_currency\":\"USD\",\"msrp_currency\":\"USD\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
