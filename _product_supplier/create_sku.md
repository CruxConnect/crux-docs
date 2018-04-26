---
title: /products/skus/
name: Create SKU
position: 12.07
visibility: public
method: post
description: Create a SKU to add to a specified item_uuid
right_code: |
  ~~~ json
  {
    "item": {
      "uuid": "2bce11c2-e60c-47a0-899b-81edfa90f666"
    },
    "sku_id": "srPycB-RNtCJpgJ-8B7FlRYo",
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
    "uuid": "7be0e3de-4108-4b08-85b4-19ddd0adcae4",
    "restrictions": "tmpunavail",
    "condition": "used",
    "distinguishing_attributes": {
      "color": "blue"
    },
    "item": {
      "uuid": "2bce11c2-e60c-47a0-899b-81edfa90f666"
    },
    "minimum_advertised_price": 40,
    "msrp": 55.99,
    "price_tiers": [],
    "product_images": [],
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

item
: (object) The Item object contains the item_uuid; the item_uuid is the parent identifer for the sku_uuid.

sku_id
: (string) The SKU Identifier for the SKU as provided by the Supplier

restrictions
: (string) The Restrictions imposed on the SKU which can include "tmpunavail" (temporary unavailable) or "discontd" (dicontinued)

condition
: (string) The Condition of the SKU; these include "new", "used", and "refurb" (refurbished)

quantity_in_stock
: (number) The Quantity In-Stock parameter indicates how many SKUs are currently available for purchase.

quantity_on_backorder
: (number) The Quantity on Backorder parameter indicates how many of this particular SKU are going to be replenished. It can be considered a tentative quantity to be added to the current quantity in-stock.

number_of_units_bundled
: (number) The Number of Units Bundled parameter indicates how many SKUs are in a single bundle.

distinguishing_attributes
: (array) The Distinguishing Attributes are attributes objects based on a category or product line may be necessary to include. It may also be empty, as per the Suppliers' discretion.


minimum_advertised_price
: (number) The Minimum Advertised Price (MAP) is a price floor for advertisement on the SKU. You may not legally list the SKU for sale at a lower price.

msrp
: (number) The Manufacturer's Suggested Retail Price for the SKU. This is only a suggestion. It is not a price floor nor is it a price ceiling.


<!-- To Be Implmented
price_tiers (TBD)
: (array) The list of Price Tier objects on this SKU including shipping_cost, minimum_tier_quantity, cost, shipping_cost_is_estimate.

product_images (TBD)
: (array) The Product Images are a list of product image objects for the SKU which contain a uuid, url, width, and height of the image.

measurements (TBD)
: (object) The Measurements object contains sku measurements object and a package measurements object.

product_identifiers (TBD)
: (object) The Product Identifiers object contains the upca, ean13, gtin14, isbn, asin, and mpn for the SKU.

catalogs (TBD)
: (array) Array of Catalog uuid(s) where the sku should reside
-->


### Response Parameters:

uuid
: (string) The Universal Unique Identifier for the SKU

restrictions
: (string) The Restrictions imposed on the SKU

condition
: (string) The Condition of the SKU; these include "new", "used", and "refurb"

distinguishing_attributes
: (object) The Distinguishing Attributes are attributes which based on a category or product line may be necessary to include. It may also be empty, as per the Suppliers' discretion.

item
: (object) The Item object contains the item_uuid; the item_uuid is the parent identifer for the sku_uuid.

minimum_advertised_price
: (number) The Minimum Advertised Price (MAP) is a price floor for advertisement on the SKU. You may not legally list the SKU for sale at a lower price.

msrp
: (number) The Manufacturer's Suggested Retail Price for the SKU. This is only a suggestion. It is not a price floor nor is it a price ceiling.

price_tiers
: (array) The list of Price Tier objects on this SKU

product_images
: (array) The Product Images are a list of product image objects for the SKU which contain a uuid, url, width, and height of the image.

measurements
: (object) The Measurements object contains sku measurements object and a package measurements object.

product_identifiers
: (object) The Product Identifiers object contains the upca, ean13, gtin14, isbn, asin, and mpn for the SKU.

catalogs
: (array) An array containing all of the catalog objects where this SKU currently resides.

created
: (string) The Created parameter indicates the date the SKU was Created in our system.

last_updated
: (string) The Last Updated parameter indicates the date the SKU was Last Updated in our system.

sku_id
: (string) The SKU Identifier for the SKU as provided by the Supplier

quantity_in_stock
: (number) The Quantity In-Stock parameter indicates how many SKUs are currently available for purchase.

quantity_on_backorder
: (number) The Quantity on Backorder parameter indicates how many of this particular SKU are going to be replenished. It can be considered a tentative quantity to be added to the current quantity in-stock.

number_of_units_bundled
: (number) The Number of Units Bundled parameter indicates how many SKUs are in a single bundle.


#### Distinguishing Attributes Object
{% include objects/attributes.md %}

#### Price Tier Object:

{% include objects/price_tier.md %}

#### Product Image Object:

uuid
: (string) The Universal Unique Identifier for the SKU Product Image

url
: (string) The URL for the SKU Product Image

width
: (number) The Image Width in pixels for the SKU Product Image

height
: (number) The Image Height in pixels for the SKU Product Image

#### SKU Measurements Object:

weight
: (number) The Weight of the SKU in the "weight_units"

weight_units
: (string) The units utilized by the supplier for weight ('g', 'kg', 'lb', and 'oz' are potential options, where 'g' is the default)

length
: (number) The Length of the SKU in "dimension_units"

width
: (number) The Width of the SKU in "dimension_units"

height
: (number) The Height of the SKU in "dimension_units"

dimension_units
: (string) The units utilized by the supplier for dimensions ('cm', 'm', 'in', and 'ft' are potential options, where 'cm' is the default)

#### Package Measurements Object:

weight
: (number) The Weight of the packaged SKU in the "weight_units"

weight_units
: (string) The units utilized by the supplier for weight ('g', 'kg', 'lb', and 'oz' are potential options, where 'g' is the default)

length
: (number) The Length of the packaged SKU in "dimension_units"

width
: (number) The Width of the packaged SKU in "dimension_units"

height
: (number) The Height of the packaged SKU in "dimension_units"

dimension_units
: (string) The units utilized by the supplier for dimensions ('cm', 'm', 'in', and 'ft' are potential options, where 'cm' is the default)

#### Product Identifiers Object:

upca
: (string) The Universal Product Code type A (UPCA) is an 11-digit code used to identify the SKU.

ean13
: (string) The 13-digit European Article Number (EAN13) also known as the International Article Number is a 13-digit code used to identify the SKU.

gtin14
: (string) The 14-digit Global Trade Identification Number (GTIN14) also known as the Global Trade Item Number is a 14-digit code used to identify the SKU.

isbn
: (string) The International Standard Book Number (ISBN) is a unique numberic commercial book identifier. If the SKU is a book or can be classified as a book in some way shape or form, then an ISBN may be available for it.

asin
: (string) Amazon Standard Identification Number (ASIN) is the unique ID provided by the Amazon company. This number may be used to identify and match this SKU up to the proper listing on Amazon.com.

mpn
: (string) Manufacturer Part Number (MPN) is an identifier given to a part by the manufacturer. This number may be used to identify products such as car parts or computer parts that generally have sofisticated systems and readily available software for product management.

#### Catalog Object

uuid
: (string) The Universal Unique Identifier for the Catalog

name
: (string) The name of the catalog

### Expected Response Codes

{% include links/response_codes.md %}


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
    "uuid": "2bce11c2-e60c-47a0-899b-81edfa90f666"
  },
  "sku_id": "srPycB-RNtCJpgJ-8B7FlRYo",
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
http --json POST 'https://api-sandbox.cruxconnect.com/products/skus/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    restrictions="tmpunavail" \
    number_of_units_bundled="2" \
    condition="used" \
    minimum_advertised_price_currency="USD" \
    item:="{
  \"uuid\": \"2bce11c2-e60c-47a0-899b-81edfa90f666\"
}" \
    sku_id="srPycB-RNtCJpgJ-8B7FlRYo" \
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
  \"uuid\": \"2bce11c2-e60c-47a0-899b-81edfa90f666\"
}" \
    sku_id="srPycB-RNtCJpgJ-8B7FlRYo" \
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
    request.write("{\"item\":{\"uuid\":\"2bce11c2-e60c-47a0-899b-81edfa90f666\"},\"sku_id\":\"srPycB-RNtCJpgJ-8B7FlRYo\",\"restrictions\":\"tmpunavail\",\"condition\":\"used\",\"quantity_in_stock\":\"500\",\"quantity_on_backorder\":\"100\",\"number_of_units_bundled\":\"2\",\"distinguishing_attributes\":{\"color\":\"blue\"},\"minimum_advertised_price\":\"40.00\",\"msrp\":\"55.99\",\"minimum_advertised_price_currency\":\"USD\",\"msrp_currency\":\"USD\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
