---
title: /products/skus/search/completion/
name: Search by Partial SKU ID
position: 4.09
visibility: internal
method: post
description: Get SKUs based on partial sku id
right_code: |
  ~~~ json
  {
    "partial": "000078"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "skus": ["TBD: Results Pending Backend Update"]
  }
  ~~~
  {: title="Response" }

---
Give a partial sku id, get matching skus in return. Used for sku id autocompletion.

### Request Parameters

partial
: (string) A partial sku id

### Response Parameters:
skus
: (array) An array of AutoCompletion SKUs objects

#### AutoCompletion SKU Object

uuid
: (string) UUID of the sku

price_tiers (TBD)
: (array) The list of Price Tier objects

supplier_uuid
: (string) UUID for the supplier to which this SKU belongs

owner_uuid
: (string)

sku_id
: (string) The SKU ID that matches

item_title
: (string) The title of the Item

distinguishing_info
: (object) Distinguishing Info for this SKU

product_images
: (array) An array of Images for this SKU

#### Price Tier Object:

{% include objects/price_tier.md %}

#### Distinguishing Info

condition
: (string) The condition of the sku. One of: new, used, refurbished

distinguishing_attributes
: (object) An object of key:value pairs. (e.g. { color: 'red', size: 9 })

number_of_units_bundled
: (number) The number of individual units bundled in this SKU

#### Image Object
uuid : (string) The Universal Unique Identifier for the Item Product Image

url
: (string) The URL for the Item Product Image

width
: (number) The Image Width in pixels for the Item Product Image

height
: (number) The Image Height in pixels for the Item Product Image

### Expected Response Codes

# Short Description
Get SKUs based on partial sku id

# Long Description
Give a partial sku id, get matching skus in return. Used for sku id autocompletion.

### Request Parameters

partial
: (string) A partial sku id

### Response Parameters:
skus
: (array) An array of AutoCompletion SKUs objects

#### AutoCompletion SKU Object

uuid
: (string) UUID of the sku

price_tiers
: (array) One or more Price Tiers

supplier_uuid
: (string) UUID for the supplier to which this SKU belongs

owner_uuid
: (string)

sku_id
: (string) The SKU ID that matches

item_title
: (string) The title of the Item

distinguishing_info
: (object) Distinguishing Info for this SKU

product_images
: (array) An array of Images for this SKU

#### Price Tier Object:
shipping_cost_is_estimate
: (bool) Is the shipping cost an estimate

minimum_tier_quantity
: (int) Minimum threshold to qualify for this tier of pricing

handling_cost
: (number) An additional charge from the supplier for handling this SKU

cost
: (number) The cost of the SKU at this price tier

shipping_cost_type
: (string) The type of shipping cost. One of: fixed, free, variable

cost_per_unit
: (number) The cost of each individual unit within a bundle

shipping_cost
: (number) The Shipping Cost per the SKU per the Price Tier

#### Distinguishing Info

condition
: (string) The condition of the sku. One of: new, used, refurbished

distinguishing_attributes
: (object) An object of key:value pairs. (e.g. { color: 'red', size: 9 })

number_of_units_bundled
: (number) The number of individual units bundled in this SKU

#### Image Object
uuid : (string) The Universal Unique Identifier for the Item Product Image

url
: (string) The URL for the Item Product Image

width
: (number) The Image Width in pixels for the Item Product Image

height
: (number) The Image Height in pixels for the Item Product Image


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/skus/search/completion/" \
     -H 'Cookie: sessionid=yzvn0w2axydrdcxc918ddbo9gcu5w3rg' \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "partial": "000078"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/skus/search/completion/' \
    'Cookie':'sessionid=yzvn0w2axydrdcxc918ddbo9gcu5w3rg' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    partial="000078"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Search by Partial SKU ID
    # POST https://api-sandbox.cruxconnect.com/products/skus/search/completion/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/skus/search/completion/",
            headers={
                "Cookie": "sessionid=yzvn0w2axydrdcxc918ddbo9gcu5w3rg",
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    partial="000078")
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
// request Search by Partial SKU ID
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/skus/search/completion/',
        method: 'POST',
        headers: {"Cookie":"sessionid=yzvn0w2axydrdcxc918ddbo9gcu5w3rg","Authorization":"Token 47d4yfbwymedhiudj384702984nakju4hajh395d","Content-Type":"application/json; charset=utf-8"}
    };
    httpOptions.headers['User-Agent'] = 'node ' + process.version;

    // Paw Store Cookies option is not supported

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
    request.write("{\"partial\":\"000078\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
