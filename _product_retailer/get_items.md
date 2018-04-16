---
title: /products/items/
name: Get Items
position: 2.18
visibility: public
method: get
description: Get Items allows you to return a complete list of items you are interested in.
right_code: |
  ~~~ json
  [
    {
      "uuid": "97fa8fdf-6b94-409e-a684-841d42605881",
      "skus": [
        {
          "uuid": "45d9c4a6-0bf0-4fa6-95df-c421ddba16e5",
          "restrictions": null,
          "condition": "new",
          "distinguishing_attributes": {},
          "minimum_advertised_price": 10.0,
          "msrp": 59.76,
          "price_tiers": [
            {
              "shipping_cost_is_estimate": false,
              "cost": 20.99,
              "shipping_cost": 1.99,
              "minimum_tier_quantity": 1
            },
            {
              "shipping_cost_is_estimate": false,
              "cost": 18.12,
              "shipping_cost": 0.99,
              "minimum_tier_quantity": 12
            },
            {
              "shipping_cost_is_estimate": false,
              "cost": 17.76,
              "shipping_cost": 0.0,
              "minimum_tier_quantity": 100
            }
          ],
          "product_images": [
            {
              "uuid": "81ada0e1-74ee-4a32-b709-745950288608",
              "url": "https://api.adorable.io/avatars/285/obad15.png",
              "width": 285,
              "height": 285
            },
            {
              "uuid": "e3817a5d-7aee-4efc-9334-14b8e5324517",
              "url": "https://api.adorable.io/avatars/80/obad24.png",
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
              "dimension_units":null
            },
            "package": {
              "weight": null,
              "length": null,
              "width": null,
              "height": null,
              "weight_units": null,
              "dimension_units":null
            }
          },
          "product_identifiers": {
            "upca": null,
            "ean13": "9780471117094",
            "gtin14": null,
            "isbn": "9780765348272",
            "asin": null,
            "mpn": null
          },
          "inventory_lists": [
            {
              "uuid": "44a1f968-1ce8-4826-9cd9-f8a54f5d542d",
              "name": "The empty calendar inventory list"
            },
            {
              "uuid": "c9b32603-f6bf-4f49-89fd-8424399974f2",
              "name": "The enchanted act inventory list"
            },
            {
              "uuid": "044a84c9-624f-49f1-bb31-29da46dd8aa9",
              "name": "The aching hook inventory list"
            }
          ],
          "created": "2017-10-23T18:26:31.098072Z",
          "last_updated": "2017-10-23T18:26:31.098115Z",
          "sku_id": "HHL59hE",
          "quantity_in_stock": 91,
          "quantity_on_backorder": 95,
          "number_of_units_bundled": 48,
          "item": {
            "uuid": "97fa8fdf-6b94-409e-a684-841d42605881"
          }
        },
      ],
      "restrict_from_marketplaces": [],
      "supplier": {
        "uuid": "f2ee86d6-7384-4144-bc35-428cd8e02c16",
        "name": "Flynn Ltd"
      },
      "cost_range": {
        "min": 17.76,
        "max": 100.12
      },
      "minimum_advertised_price_range": {
        "min": 10.0,
        "max": 10.0
      },
      "msrp_range": {
        "min": 59.76,
        "max": 173.04
      },
      "product_images": [
        {
          "uuid": "602a19a4-7ac8-480c-ab19-ee981051f742",
          "url": "https://api.adorable.io/avatars/80/obad21.png",
          "width": 80,
          "height": 80
        },
        {
          "uuid": "8e6e1355-a185-4574-bb54-dc2193b9ab2d",
          "url": "https://api.adorable.io/avatars/285/obad39.png",
          "width": 285,
          "height": 285
        }
      ],
      "created": "2017-10-23T18:26:31.047335Z",
      "last_updated": "2017-10-23T18:26:31.047384Z",
      "item_id": "1hNAnG3JLvkLOiv",
      "title": "The changeable soap item",
      "description": "Underneath all that indelible trees there will be changeable soap item. Watching. Waiting. Wanting. Wishing. Wondering. Our changeable soap item comes with built-in bait for that extra abrupt flavor. There's just something accessible about cuddling up with your own changeable soap item! changeable soap item works best when you give it plenty of TLC. All your wildest dreams would come true. Because if your changeable soap item is bold, childlike, and beautiful, everyone will think that of your room, too! And that's why you don't put the walk inside your changeable soap item. It doesn't work that way. And then there's our changeable soap item, which will blow off your instinctive walk!!",
      "warranty": "A entire warranty",
      "return_policy": null,
      "manufacturer": "government Corp.",
      "brand": "water brand",
      "country_of_origin": "SB",
      "shipping_origin_country": "CM",
      "other_marketplace_restriction": null,
      "fba_certified": null,
      "custom_attributes": {
        "diameter": 1,
        "hair-color": "brunette"
      },
      "categories": [
        45
      ]
    },
  ]
  ~~~
  {: title="Response" }

---
Get Items allows you to return a complete list of items you are interested in.

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

# Expected Response Codes

{% include links/response_codes.md %}

~~~ bash
curl "https://api-sandbox.cruxconnect.com/products/items/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/products/items/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Item List
    # GET https://api-sandbox.cruxconnect.com/products/items/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/products/items/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
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
// request Get Item List
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/items/',
        method: 'GET',
        headers: {"Authorization":"Token 47d4yfbwymedhiudj384702984nakju4hajh395d","Content-Type":"application/json; charset=utf-8"}
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
