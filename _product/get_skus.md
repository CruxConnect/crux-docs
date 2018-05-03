---
title: /products/skus/
name: Get SKUs
position: 4.08
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
          "width": 285,
          "height": 285
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
: (list) The list of Price Tier objects on this SKU

product_images
: (list) The Product Images are a list of product image objects for the SKU which contain a uuid, url, width, and height of the image.

measurements
: (object) The Measurements object contains sku measurements object and a package measurements object.

product_identifiers
: (object) The Product Identifiers object contains the upca, ean13, gtin14, isbn, asin, and mpn for the SKU.

inventory_lists
: (list) The Inventory Lists list contains all of the Inventory List objects where this SKU currently resides.

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
: (number) The Weight of the packaged SKU in "weight_units"

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

#### Inventory List Object:

uuid
: (string) The Universal Unique Identifier for the Inventory List

name
: (string) The Name your company has given to this Inventory List

Supplier Object:

uuid
: (string) The Universal Unique Identifier for the Supplier

name
: (string) The Supplier Name

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
