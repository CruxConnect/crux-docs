---
title: /api/products/items/
name: Create Item - Supplier
position: 2.19
type: post
description: Create Items allows you to create (add) an item in a Supplier account
right_code: |
  ~~~ json
  {
    "item_id": "RtfiaeIRXj",
    "title": "The Item Title - XkuKRGySts",
    "description": "This is the default description. In this description the product is explained in detail. The idea with the description is to include everything that isn't already included elsewhere in the item attributes, such as manufacturer, brand, country_of_origin, shipping_origin_country, marketplace_restrictions, fba_certified, etc.",
    "warranty": "The warranty information is included here",
    "return_policy": "The return policy is included here",
    "manufacturer": "The Manufacturer",
    "brand": "The Brand",
    "country_of_origin": "CN",
    "shipping_origin_country": "US",
    "other_marketplace_restriction": "eBay, Amazon, Sears, Walmart",
    "fba_certified": false,
    "custom_attributes": {
      "Color": "black",
      "Size": "15\" x 15\" x 18\""
    }
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "4cc9a5f6-e024-4f48-8775-7ff35543f520",
    "skus": [],
    "restrict_from_marketplaces": null,
    "supplier": {
      "uuid": "9ff4ca63-7a46-4eee-a4fb-859e201460c8",
      "name": "projectzuul"
    },
    "cost_range": {
      "min": null,
      "max": null
    },
    "minimum_advertised_price_range": {
      "min": null,
      "max": null
    },
    "msrp_range": {
      "min": null,
      "max": null
    },
    "product_images": [],
    "created": "2017-11-07T16:16:55.106356Z",
    "last_updated": "2017-11-07T16:16:55.106410Z",
    "item_id": "lWWISBERmJ",
    "title": "The Item Title - KaiEHTsqXH",
    "description": "This is the default description. In this description the product is explained in detail. The idea with the description is to include everything that isn't already included elsewhere in the item attributes, such as manufacturer, brand, country_of_origin, shipping_origin_country, marketplace_restrictions, fba_certified, etc.",
    "warranty": "The warranty information is included here",
    "return_policy": "The return policy is included here",
    "manufacturer": "The Manufacturer",
    "brand": "The Brand",
    "country_of_origin": "CN",
    "shipping_origin_country": "US",
    "other_marketplace_restriction": "eBay, Amazon, Sears, Walmart",
    "fba_certified": false,
    "custom_attributes": {
      "Color": "black",
      "Size": "15\" x 15\" x 18\""
    },
    "categories": []
  }
  ~~~
  {: title="Response" }

---
Create Items allows you to create (add) an item in a Supplier account. By providing  Your username and password are optional as you can send your authorization token to receive this information.

URL Endpoint: /api/products/items/

### Request Parameters:

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
: (object) The Custom Attributes object parameter contains any special attributes you would like to include in a key-value pair

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
curl -X "POST" "https://stable.projectthanos.com/api/products/items/" \
     -H 'Authorization: Token 0102f963bf7c4c4452d46e30645de9182ba0d137' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "description": "This is the default description. In this description the product is explained in detail. The idea with the description is to include everything that isn'"'"'t already included elsewhere in the item attributes, such as manufacturer, brand, country_of_origin, shipping_origin_country, marketplace_restrictions, fba_certified, etc.",
  "shipping_origin_country": "US",
  "country_of_origin": "CN",
  "item_id": "RtfiaeIRXj",
  "brand": "The Brand",
  "other_marketplace_restriction": "eBay, Amazon, Sears, Walmart",
  "fba_certified": false,
  "title": "The Item Title - XkuKRGySts",
  "custom_attributes": {
    "Color": "black",
    "Size": "15\\" x 15\\" x 18\\""
  },
  "warranty": "The warranty information is included here",
  "manufacturer": "The Manufacturer",
  "return_policy": "The return policy is included here"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://stable.projectthanos.com/api/products/items/' \
    'Authorization':'Token 0102f963bf7c4c4452d46e30645de9182ba0d137' \
    'Content-Type':'application/json; charset=utf-8' \
    description="This is the default description. In this description the product is explained in detail. The idea with the description is to include everything that isn't already included elsewhere in the item attributes, such as manufacturer, brand, country_of_origin, shipping_origin_country, marketplace_restrictions, fba_certified, etc." \
    shipping_origin_country="US" \
    country_of_origin="CN" \
    item_id="RtfiaeIRXj" \
    brand="The Brand" \
    other_marketplace_restriction="eBay, Amazon, Sears, Walmart" \
    fba_certified:=false \
    title="The Item Title - XkuKRGySts" \
    custom_attributes:="{
  \"Color\": \"black\",
  \"Size\": \"15\\\" x 15\\\" x 18\\\"\"
}" \
    warranty="The warranty information is included here" \
    manufacturer="The Manufacturer" \
    return_policy="The return policy is included here"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Create Item - Supplier
    # POST https://stable.projectthanos.com/api/products/items/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/products/items/",
            headers={
                "Authorization": "Token 0102f963bf7c4c4452d46e30645de9182ba0d137",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    description="This is the default description. In this description the product is explained in detail. The idea with the description is to include everything that isn't already included elsewhere in the item attributes, such as manufacturer, brand, country_of_origin, shipping_origin_country, marketplace_restrictions, fba_certified, etc." \
    shipping_origin_country="US" \
    country_of_origin="CN" \
    item_id="RtfiaeIRXj" \
    brand="The Brand" \
    other_marketplace_restriction="eBay, Amazon, Sears, Walmart" \
    fba_certified:=false \
    title="The Item Title - XkuKRGySts" \
    custom_attributes:="{
  \"Color\": \"black\",
  \"Size\": \"15\\\" x 15\\\" x 18\\\"\"
}" \
    warranty="The warranty information is included here" \
    manufacturer="The Manufacturer" \
    return_policy="The return policy is included here")
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
// request Create Item - Supplier
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/products/items/',
        method: 'POST',
        headers: {"Authorization":"Token 0102f963bf7c4c4452d46e30645de9182ba0d137","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"item_id\":\"RtfiaeIRXj\",\"title\":\"The Item Title - XkuKRGySts\",\"description\":\"This is the default description. In this description the product is explained in detail. The idea with the description is to include everything that isn't already included elsewhere in the item attributes, such as manufacturer, brand, country_of_origin, shipping_origin_country, marketplace_restrictions, fba_certified, etc.\",\"warranty\":\"The warranty information is included here\",\"return_policy\":\"The return policy is included here\",\"manufacturer\":\"The Manufacturer\",\"brand\":\"The Brand\",\"country_of_origin\":\"CN\",\"shipping_origin_country\":\"US\",\"other_marketplace_restriction\":\"eBay, Amazon, Sears, Walmart\",\"fba_certified\":false,\"custom_attributes\":{\"Color\":\"black\",\"Size\":\"15\\\" x 15\\\" x 18\\\"\"}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
