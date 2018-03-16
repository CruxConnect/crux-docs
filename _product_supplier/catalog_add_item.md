---
title: /products/catalogs/&ltcatalog-uuid&gt/add-items/
name: Catalog Add Item
position: 2.04
visibility: public
method: post
description: Add already existing Items to a Catalog
right_code: |
  ~~~ json
  {
    "item_uuids": [
      "fc82cac4-391b-4fab-a335-fe8867494750"
    ]
  }
  ~~~
  {: title="Request" }


---
Add already existing Items to a Catalog for Retailers to access. This allows you to add Items to a Catalog with all associated SKUs. By providing your catalog_uuid and a list of item_ids with related data, you can successfully add them to the indicated Catalog.Your username and password are optional as you can send your authorization token to receive this information.

URL Endpoint: /api/products/catalogs/<catalog_uuid>/add-items/

### Request Parameters:

item_uuids
: (array) The Item UUIDs array parameter holds item_uuids for all of the items you wish to add to your Catalog

#### Item ID Object:

item_id
: (string) The Item Identifier is the identifier for the item as provided by the supplier. This is the parent identifier for the child SKU; SKUs are considered children identifiers to the item_id.

skus
: (array) The Stock Keeping Units (SKUs) array contains individual SKUs, or Item-variants, with their SKU-level data

restrict_from_marketplaces
: (array) The Restrict From Marketplaces parameter indicates the marketplaces where sales for this Item are not permitted

cost_range
: (object) The Cost Range object contains the minimum and maximum prices you will pay for the Item, based on the available variants (SKUs).

minimum_advertised_price_range
: (object) The Minimum Advertised Price Range object contains the minimum and maximum MAPs for the item, based on the available variants (SKUs).

msrp_range
: (object) The Manufacturer's Suggested Retail Price Range object contains the minimum and maximum MSRPs for the Item, based on the available variants (SKUs).

product_images
: (array) The Product Images array stores a array of images for the item, based on the available variants (SKUs)

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
: (array) The Categories array contains a list of the categories, as provided by the Supplier, for this Item.

#### SKU Object:

sku_id
: (string) The SKU Identifier for the SKU as provided by the Supplier

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
: (array) The array of Price Tier objects on this SKU including shipping_cost, minimum_tier_quantity, cost, shipping_cost_is_estimate.

product_images
: (array) The Product Images are a array of product image objects for the SKU which contain a uuid, url, width, and height of the image.

measurements
: (object) The Measurements object contains sku measurements object and a package measurements object.

product_identifiers
: (object) The Product Identifiers object contains the upca, ean13, gtin14, isbn, asin, and mpn for the SKU.

inventory_lists
: (array) The Inventory Lists array contains all of the Inventory array objects where this SKU currently resides.

created
: (string) The Created parameter indicates the date the SKU was Created in our system.

last_updated
: (string) The Last Updated parameter indicates the date the SKU was Last Updated in our system.

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

url
: (string) The URL for the SKU Product Image

width
: (number) The Image Width in pixels for the SKU Product Image

height
: (number) The Image Height in pixels for the SKU Product Image

#### SKU Measurements Object:

weight
: (number) The Weight of the SKU in pounds (lbs.)

length
: (number) The Length of the SKU in inches

width
: (number) The Width of the SKU in inches

height
: (number) The Height of the SKU in inches

#### Package Measurements Object:

weight
: (number) The Weight of the packaged SKU in pounds (lbs.)

length
: (number) The Length of the packaged SKU in inches

width
: (number) The Width of the packaged SKU in inches

height
: (number) The Height of the packaged SKU in inches

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

Manufacturer's Suggested Retail Price (MSRP) Range Object:

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

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/catalogs/b1a6513c-d624-4f33-9a59-6f6c670cf280/add-items/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "item_uuids": [
    "fc82cac4-391b-4fab-a335-fe8867494750"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/catalogs/b1a6513c-d624-4f33-9a59-6f6c670cf280/add-items/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    item_uuids:="[
  \"fc82cac4-391b-4fab-a335-fe8867494750\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Catalog Add Item
    # POST https://api-sandbox.cruxconnect.com/products/catalogs/b1a6513c-d624-4f33-9a59-6f6c670cf280/add-items/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/catalogs/b1a6513c-d624-4f33-9a59-6f6c670cf280/add-items/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    item_uuids:="[
  \"fc82cac4-391b-4fab-a335-fe8867494750\"
]")
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
// request Catalog Add Item
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/catalogs/b1a6513c-d624-4f33-9a59-6f6c670cf280/add-items/',
        method: 'POST',
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
    request.write("{\"item_uuids\":[\"fc82cac4-391b-4fab-a335-fe8867494750\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
