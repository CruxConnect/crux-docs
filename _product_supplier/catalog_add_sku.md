---
title: /products/catalogs/f2f8273a-18c4-44d8-820f-7404bd4f0589/add-skus/
name: Catalog Add SKU
position: 2.03
method: post
description: Add already existing SKUs to a Catalog
right_code: |
  ~~~ json
  {
    "sku_uuids": [
      "84d075e0-28e2-449c-9292-5cfe6981e922"
    ]
  }
  ~~~
  {: title="Request" }


---
Add already existing SKUs to a Catalog for Retailers to access. This allows you to add SKUs to a Catalog. By providing your catalog_uuid, and a list of sku_uuids with related data, you can successfully add them to the items added previously to the indicated Catalog.Your username and password are optional as you can send your authorization token to receive this information.

URL Endpoint: /products/catalogs/<catalog_uuid>/add-skus/

### Request Parameters:

sku_uuids
: (list) The SKU UUIDs list parameter holds a list of sku_uuids to an existing catalog

#### SKU ID Object:

sku_id
: (string) The SKU Identifier for the SKU

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
curl -X "POST" "https:/.cruxconnect.com/products/catalogs/f2f8273a-18c4-44d8-820f-7404bd4f0589/add-skus/" \
     -H 'Authorization: Token 825dd305b5858e2373763ff338615db822fe67a0' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "sku_uuids": [
    "84d075e0-28e2-449c-9292-5cfe6981e922"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https:/.cruxconnect.com/products/catalogs/f2f8273a-18c4-44d8-820f-7404bd4f0589/add-skus/' \
    'Authorization':'Token 825dd305b5858e2373763ff338615db822fe67a0' \
    'Content-Type':'application/json; charset=utf-8' \
    sku_uuids:="[
  \"84d075e0-28e2-449c-9292-5cfe6981e922\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Catalog Add SKU
    # POST https:/.cruxconnect.com/products/catalogs/f2f8273a-18c4-44d8-820f-7404bd4f0589/add-skus/

    try:
        response = requests.post(
            url="https:/.cruxconnect.com/products/catalogs/f2f8273a-18c4-44d8-820f-7404bd4f0589/add-skus/",
            headers={
                "Authorization": "Token 825dd305b5858e2373763ff338615db822fe67a0",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    sku_uuids:="[
  \"84d075e0-28e2-449c-9292-5cfe6981e922\"
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
// request Catalog Add SKU
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api.cruxconnect.com',
        port: '443',
        path: '/products/catalogs/f2f8273a-18c4-44d8-820f-7404bd4f0589/add-skus/',
        method: 'POST',
        headers: {"Authorization":"Token 825dd305b5858e2373763ff338615db822fe67a0","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"sku_uuids\":[\"84d075e0-28e2-449c-9292-5cfe6981e922\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
