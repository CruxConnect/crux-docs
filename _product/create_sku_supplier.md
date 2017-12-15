---
title: /api/products/skus/
name: Create SKU - Supplier
position: 2.24
type: post
description: Create a SKU to add to a specified item_uuid
right_code: |
  ~~~ json
  {
    "item": {
      "uuid": "4cc9a5f6-e024-4f48-8775-7ff35543f520"
    },
    "sku_id": "AWWghwmTNb",
    "minimum_advertised_price": "40.00",
    "msrp": "55.99",
    "quantity_in_stock": "500",
    "quantity_on_backorder": "100",
    "number_of_units_bundled": "2",
    "minimum_advertised_price_currency": "USD",
    "msrp_currency": "USD"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "b0a7e210-ebb5-460d-a75a-6d417899aedb",
    "restrictions": null,
    "condition": "new",
    "distinguishing_attributes": {},
    "item": {
      "uuid": "4cc9a5f6-e024-4f48-8775-7ff35543f520"
    },
    "minimum_advertised_price": 40,
    "msrp": 55.99,
    "price_tiers": [],
    "product_images": [],
    "measurements": {
      "sku": {
        "weight": null,
        "length": null,
        "width": null,
        "height": null
      },
      "package": {
        "weight": null,
        "length": null,
        "width": null,
        "height": null
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
        "uuid": "962900df-0bd3-447b-9bdd-caff66a14591",
        "name": "master"
      }
    ],
    "created": "2017-11-07T19:16:46.151007Z",
    "last_updated": "2017-11-07T19:16:46.151057Z",
    "sku_id": "RcKrkPpsgC",
    "quantity_in_stock": 500,
    "quantity_on_backorder": 100,
    "number_of_units_bundled": 2,
    "minimum_advertised_price_currency": "USD",
    "msrp_currency": "USD"
  }
  ~~~
  {: title="Response" }

---
Create a SKU to add to a specified item_uuid.

URL Endpoint: /api/products/skus/

### Request Parameters:

item
: (object) The Item object contains the item_uuid; the item_uuid is the parent identifer for the sku_uuid.

sku_id
: (string) The SKU Identifier for the SKU as provided by the Supplier

minimum_advertised_price
: (number) The Minimum Advertised Price (MAP) is a price floor for advertisement on the SKU. You may not legally list the SKU for sale at a lower price.

msrp
: (number) The Manufacturer's Suggested Retail Price for the SKU. This is only a suggestion. It is not a price floor nor is it a price ceiling.

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
curl -X "POST" "https://stable.projectthanos.com/api/products/skus/" \
     -H 'Authorization: Token 0102f963bf7c4c4452d46e30645de9182ba0d137' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "sku_id": "AWWghwmTNb",
  "minimum_advertised_price": "40.00",
  "msrp_currency": "USD",
  "quantity_in_stock": "500",
  "quantity_on_backorder": "100",
  "number_of_units_bundled": "2",
  "msrp": "55.99",
  "item": {
    "uuid": "4cc9a5f6-e024-4f48-8775-7ff35543f520"
  },
  "minimum_advertised_price_currency": "USD"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://stable.projectthanos.com/api/products/skus/' \
    'Authorization':'Token 0102f963bf7c4c4452d46e30645de9182ba0d137' \
    'Content-Type':'application/json; charset=utf-8' \
    sku_id="AWWghwmTNb" \
    minimum_advertised_price="40.00" \
    msrp_currency="USD" \
    quantity_in_stock="500" \
    quantity_on_backorder="100" \
    number_of_units_bundled="2" \
    msrp="55.99" \
    item:="{
  \"uuid\": \"4cc9a5f6-e024-4f48-8775-7ff35543f520\"
}" \
    minimum_advertised_price_currency="USD"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Create SKU - Supplier
    # POST https://stable.projectthanos.com/api/products/skus/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/products/skus/",
            headers={
                "Authorization": "Token 0102f963bf7c4c4452d46e30645de9182ba0d137",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    sku_id="AWWghwmTNb" \
    minimum_advertised_price="40.00" \
    msrp_currency="USD" \
    quantity_in_stock="500" \
    quantity_on_backorder="100" \
    number_of_units_bundled="2" \
    msrp="55.99" \
    item:="{
  \"uuid\": \"4cc9a5f6-e024-4f48-8775-7ff35543f520\"
}" \
    minimum_advertised_price_currency="USD")
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
// request Create SKU - Supplier
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/products/skus/',
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
    request.write("{\"item\":{\"uuid\":\"4cc9a5f6-e024-4f48-8775-7ff35543f520\"},\"sku_id\":\"AWWghwmTNb\",\"minimum_advertised_price\":\"40.00\",\"msrp\":\"55.99\",\"quantity_in_stock\":\"500\",\"quantity_on_backorder\":\"100\",\"number_of_units_bundled\":\"2\",\"minimum_advertised_price_currency\":\"USD\",\"msrp_currency\":\"USD\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
