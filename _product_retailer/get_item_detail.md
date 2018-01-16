---
title: /products/items/&ltitem_uuid&gt/
name: Get Item Detail
position: 2.20
method: get
description: Get Details about an Item and the SKUs associated to it.
right_code: |
  ~~~ json
  {
    "uuid": "0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017",
    "skus": [
      {
        "uuid": "a81dc78b-6af2-461c-8a26-6e8d8a3e8b46",
        "restrictions": null,
        "condition": "refurb",
        "distinguishing_attributes": {
          "size": 9,
          "color": "indigo"
        },
        "minimum_advertised_price": 10,
        "msrp": 53.95,
        "price_tiers": [
          {
            "shipping_cost_is_estimate": true,
            "shipping_cost": 1.99,
            "cost": 100.12,
            "minimum_tier_quantity": 2
          },
          {
            "shipping_cost_is_estimate": true,
            "shipping_cost": 0.99,
            "cost": 75.6,
            "minimum_tier_quantity": 4
          }
        ],
        "product_images": [
          {
            "uuid": "800388e7-de33-494a-94ac-93f57f959de3",
            "url": "https:/.adorable.io/avatars/80/obad15.png",
            "width": 80,
            "height": 80
          },
          {
            "uuid": "bd465a5a-c006-45b9-ac26-83fd978ba36f",
            "url": "https:/.adorable.io/avatars/80/obad33.png",
            "width": 80,
            "height": 80
          }
        ],
        "measurements": {
          "sku": {
            "weight": null,
            "length": null,
            "width": null,
            "height": null,
            "weight_units": null,
            "dimension_units": null
          },
          "package": {
            "weight": null,
            "length": null,
            "width": null,
            "height": null,
            "weight_units": null,
            "dimension_units": null
          }
        },
        "product_identifiers": {
          "upca": null,
          "ean13": "4006381333931",
          "gtin14": null,
          "isbn": "0765348276",
          "asin": null,
          "mpn": null
        },
        "inventory_lists": [
          {
            "uuid": "c9b32603-f6bf-4f49-89fd-8424399974f2",
            "name": "The enchanted act inventory list"
          },
          {
            "uuid": "8676b377-4180-4ad9-b71d-dccfa83bea43",
            "name": "Nicks List"
          }
        ],
        "created": "2017-10-23T18:28:07.217708Z",
        "last_updated": "2017-10-23T18:28:07.217751Z",
        "sku_id": "KzQRPs",
        "quantity_in_stock": 59,
        "quantity_on_backorder": null,
        "number_of_units_bundled": 1,
        "minimum_advertised_price_currency": "USD",
        "msrp_currency": "USD",
        "item": {
          "uuid": "0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017"
        }
      },
      {
        "uuid": "33d478dc-1a34-472c-84ee-3e7aec7b35f3",
        "restrictions": null,
        "condition": "refurb",
        "distinguishing_attributes": {
          "size": 12,
          "color": "black"
        },
        "minimum_advertised_price": 10,
        "msrp": 89.03,
        "price_tiers": [
          {
            "shipping_cost_is_estimate": true,
            "shipping_cost": 1.99,
            "cost": 100.12,
            "minimum_tier_quantity": 2
          },
          {
            "shipping_cost_is_estimate": true,
            "shipping_cost": 0.99,
            "cost": 75.6,
            "minimum_tier_quantity": 4
          },
          {
            "shipping_cost_is_estimate": true,
            "shipping_cost": 0,
            "cost": 49.99,
            "minimum_tier_quantity": 16
          }
        ],
        "product_images": [
          {
            "uuid": "38a566f9-7cd1-4d0a-8d99-c12bd749bd78",
            "url": "https:/.adorable.io/avatars/285/obad24.png",
            "width": 285,
            "height": 285
          },
          {
            "uuid": "74bef732-c204-43af-97a6-bee4e2d0997b",
            "url": "https:/.adorable.io/avatars/155/obad20.png",
            "width": 155,
            "height": 155
          }
        ],
        "measurements": {
          "sku": {
            "weight": null,
            "length": null,
            "width": null,
            "height": null,
            "weight_units": null,
            "dimension_units": null
          },
          "package": {
            "weight": null,
            "length": null,
            "width": null,
            "height": null,
            "weight_units": null,
            "dimension_units": null
          }
        },
        "product_identifiers": {
          "upca": null,
          "ean13": null,
          "gtin14": "71123456000016",
          "isbn": null,
          "asin": "0000000000",
          "mpn": null
        },
        "inventory_lists": [
          {
            "uuid": "c9b32603-f6bf-4f49-89fd-8424399974f2",
            "name": "The enchanted act inventory list"
          },
          {
            "uuid": "8676b377-4180-4ad9-b71d-dccfa83bea43",
            "name": "Nicks List"
          },
          {
            "uuid": "164aaf12-2400-4af7-b5c1-00da17c3f60e",
            "name": "New Test Inventory List Name Py8AXVk2upqoUebbR3MKrt6vnSxqq3PD"
          }
        ],
        "created": "2017-10-23T18:28:07.945769Z",
        "last_updated": "2017-10-23T18:28:07.945815Z",
        "sku_id": "khUyhMFBWSy35",
        "quantity_in_stock": 32,
        "quantity_on_backorder": 61,
        "number_of_units_bundled": 48,
        "minimum_advertised_price_currency": "USD",
        "msrp_currency": "USD",
        "item": {
          "uuid": "0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017"
        }
      }
    ],
    "restrict_from_marketplaces": [],
    "supplier": {
      "uuid": "ce4f9803-7870-4a78-b2cb-8949c8f550d6",
      "name": "Underwood-Chavez"
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
      "max": 165.45,
      "min": 53.95
    },
    "product_images": [
      {
        "uuid": "443ba02e-973b-4fee-8a00-9c4bd8c5c3a5",
        "url": "https:/.adorable.io/avatars/80/obad21.png",
        "width": 80,
        "height": 80
      },
      {
        "uuid": "b08c80af-7b64-47e7-ab49-e77c8a5b33d7",
        "url": "https:/.adorable.io/avatars/80/obad20.png",
        "width": 80,
        "height": 80
      }
    ],
    "created": "2017-10-23T18:28:07.156739Z",
    "last_updated": "2017-10-23T18:28:07.156782Z",
    "item_id": "G5kZl9ujiiXlD4c9Z",
    "title": "The capital arch item",
    "description": "Oh, no you don't!  Our capital arch item kicks the caring competition in the recess! Our capital arch item comes with built-in base for that extra chemical flavor. And then there's our capital arch item, which will blow off your enthusiastic hose!! Be the kind of person your mother wanted you to me. Because we care about how your capital arch item looks! You know you want it. Because if your capital arch item is bold, elaborate, and beautiful, everyone will think that of your swim, too! And that's why you don't put the test inside your capital arch item. It doesn't work that way. I like, it, I love it, I want some more of it.",
    "warranty": "A certain warranty",
    "return_policy": null,
    "manufacturer": "pizzas Corp.",
    "brand": "base brand",
    "country_of_origin": "BV",
    "shipping_origin_country": "NZ",
    "other_marketplace_restriction": null,
    "fba_certified": null,
    "custom_attributes": {
      "hair-color": "black",
      "diameter": 1
    },
    "categories": [
      66
    ]
  }
  ~~~
  {: title="Response" }

---
Get Details about an Item and the SKUs associated to it. There is a varying amount of data provided with each item and associated SKUs. The Response Parameters listed below are potential attributes of Items and SKUs that may be returned to you.

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Item

skus
: (list) The Stock Keeping Units (SKUs) list contains individual SKUs, or Item-variants, with their SKU-level data

restrict_from_marketplaces
: (list) The Restrict From Marketplaces parameter indicates the marketplaces where sales for this Item are not permitted

supplier
: (object) The Supplier object contains the uuid for the Supplier and the Supplier name

cost_range
: (object) The Cost Range object contains the minimum and maximum prices you will pay for the Item, based on the available variants (SKUs).

minimum_advertised_price_range
: (object) The Minimum Advertised Price Range object contains the minimum and maximum MAPs for the item, based on the available variants (SKUs).

msrp_range
: (object) The Manufacturer's Suggested Retail Price Range object contains the minimum and maximum MSRPs for the Item, based on the available variants (SKUs).

product_images
: (list) The Product Images list stores a list of images for the item, based on the available variants (SKUs)

created
: (string) The Created parameter is the date when the Item was added to our system.

last_updated
: (string) The Last Updated parameter is the date when the Item was last updated in our system.

item_id
: (string) The Item Identifier is the identifier for the item as provided by the supplier. This is the parent identifier for the child SKU; SKUs are considered children identifiers to the item_id.

title
: (string) The Item Title is the title for the Item

description
: (string) The Description for the Item

warranty
: (string) The Warranty for the Item, if provided/available

return_policy
: (string) The Return Policy for the Item, if provided/available

manufacturer
: (string) The Manufacturer for the Item

brand
: (string) The Brand of the Item

country_of_origin
: (string) The Country of Origin is the country code of the origin of the Item

shipping_origin_country
: (string) The Shipping Origin Country is the country code of the shipping origin of the Item. If the item is manufacturered in the USA, but the distributor is in Canada, the Shipping Origin Country is going to have a value of "CA".

other_marketplace_restriction
: (string) The Other Markeplace Restriction is a string list of markeplaces where the item is prohibited from being sold.

fba_certified
: (boolean) The Fulfillment By Amazon (FBA) Certified parameter indicates whether this supplier has FBA set up on this Item.

custom_attributes
: (object) The Custom Attributes object contains any special or custom-created attributes provided by the Supplier for this Item.

categories
: (list) The Categories list contains a list of the categories, as provided by the Supplier, for this Item.

#### SKU Object:

uuid
: (string) The Universal Unique Identifier for the SKU

restrictions
: (string) The Restrictions imposed on the SKU

condition
: (string) The Condition of the SKU; these include "new", "used", and "refurb"

distinguishing_attributes
: (object) The Distinguishing Attributes are attributes which based on a category or product line may be necessary to include. It may also be empty, as per the Suppliers' discretion.

minimum_advertised_price
: (number) The Minimum Advertised Price (MAP) is a price floor for advertisement on the SKU. You may not legally list the SKU for sale at a lower price.

msrp
: (number) The Manufacturer's Suggested Retail Price for the SKU. This is only a suggestion. It is not a price floor nor is it a price ceiling.

price_tiers
: (list) The list of Price Tier objects on this SKU including shipping_cost, minimum_tier_quantity, cost, shipping_cost_is_estimate.

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

minimum_advertised_price_currency
: (string) The Minimum Advertised Price Currency parameter indicates what currency the MAP is based on.

msrp_currency
: (string) The Manufacturer's Suggested Retail Price Currency parameter indicates what currency the MSRP is based on.

item
: (object) The Item object contains the item_uuid; the item_uuid is the parent identifer for the sku_uuid.

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

#### Supplier Object:

uuid
: (string) The Universal Unique Identifier for the Supplier

name
: (string) The Supplier Name

#### Cost Range Object:

min
: (number) The Minimum price for one of the SKUs or Item-variants

max
: (number) The Maximum price for one of the SKUs or Item-variants

#### Minimum Advertized Price Range Object:

min
: (number) The Minimum MAP for one of the SKUs or Item-variants

max
: (number) The Maximum MAP for one of the SKUs or Item-variants

#### Manufacturer's Suggested Retail Price (MSRP) Range Object:

min
: (number) The Minimum MSRP for one of the SKUs or Item-variants

max
: (number) The Maximum MSRP for one of the SKUs or Item-variants

#### Item Product Images Object:

uuid
: (string) The Universal Unique Identifier for the Item Product Image

url
: (string) The URL for the Item Product Image

width
: (number) The Image Width in pixels for the Item Product Image

height
: (number) The Image Height in pixels for the Item Product Image

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
curl "https:/.cruxconnect.com/products/items/0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https:/.cruxconnect.com/products/items/0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Item Detail
    # GET https:/.cruxconnect.com/products/items/0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017/

    try:
        response = requests.get(
            url="https:/.cruxconnect.com/products/items/0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
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
// request Get Item Detail
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api.cruxconnect.com',
        port: '443',
        path: '/products/items/0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017/',
        method: 'GET',
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
