---
title: /timp/products/items/
name: Create Item
position: 11.02
visibility: public
method: post
description: Create Items allows you to create (add) an item in a Supplier account
right_code: |
  ~~~ json
  {
    "item_id": "J2b35VAXEumkduUhm5ik3MlQ6AS55UgE",
    "title": "The Item Title - GeUHLUfHYx",
    "description": "This is the default description. In this description the product is explained in detail. The idea with the description is to include everything that isn't already included elsewhere in the item attributes, such as manufacturer, brand, country_of_origin, shipping_origin_country, marketplace_restrictions, fba_certified, etc.",
    "warranty": "The warranty information is included here",
    "return_policy": "The return policy is included here",
    "manufacturer": "The Manufacturer",
    "brand": "The Brand",
    "country_of_origin": "CN",
    "shipping_origin_country": "US",
    "other_marketplace_restriction": "eBay, Amazon, Sears, Walmart",
    "fba_certified": false,
    "category_id": "8hVEcErHcJToqARWeITB6yvdmrXsbH6x",
    "custom_attributes": {
      "Color": "black",
      "Size": "XL"
    },
    "categories": [
      {
        "path": [
          "computer",
          "games"
        ]
      }
    ]
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "905c3e4b-ef10-4f77-b07e-03d4ecb743a0",
    "skus": [],
    "restrict_from_marketplaces": null,
    "supplier": {
      "uuid": "ed0eb521-1a0a-4526-a155-31daa726e66c",
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
    "product_videos": [],
    "categories": [
      {
        "uuid": "b010fd20-751e-4fe1-b511-a194d1ca40b9",
        "path": [
          "computer",
          "games"
        ],
        "description": ""
      }
    ],
    "created": "2018-08-24T21:55:16.877922Z",
    "last_updated": "2018-08-24T21:55:16.877972Z",
    "item_id": "00lm4MAHOgppj2Vg8EoLhx7e3MyICdnM",
    "title": "The Item Title - ldRQfxUITI",
    "description": "This is the default description. In this description the product is explained in detail. The idea with the description is to include everything that isn't already included elsewhere in the item attributes, such as manufacturer, brand, country_of_origin, shipping_origin_country, marketplace_restrictions, fba_certified, etc.",
    "warranty": "The warranty information is included here",
    "return_policy": "The return policy is included here",
    "manufacturer": "The Manufacturer",
    "brand": "The Brand",
    "country_of_origin": "CN",
    "shipping_origin_country": "US",
    "other_marketplace_restriction": "eBay, Amazon, Sears, Walmart",
    "fba_certified": false,
    "item_attributes": {}
  }
  ~~~
  {: title="Response" }

---
Create Items allows you to create (add) an item in a Supplier account. By providing the required request parameters you may create a new item.

Note: this endpoint is under development.  There are a number of fields in the response that may not yet be setable in the request body that are returned in the response.

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

categories
: (array) The Categories array contains objects that describe the path to the item.  It is structured like categories=[{'path': ['home', 'garden']}] where the item would exist in the garden category which has home as it's parent. Not implemented yet is passing in the category path description, although a blank description is passed back in the response.

custom_attributes
: (object) The Custom Attributes object parameter contains any special attributes you would like to include in a key-value pair


### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Item

skus
: (array) The Stock Keeping Units (SKUs) is returned as an empty array that will be used to contains individual SKUs, or Item-variants, with their SKU-level data.  [see Create Sku](#product_suppliercreate_sku)

restrict_from_marketplaces
: (array) The Restrict From Marketplaces parameter indicates the marketplaces where sales for this Item are not permitted

supplier
: (object) The Supplier object contains the uuid for the Supplier and the Supplier name

cost_range
: (object) The Cost Range object contains the minimum and maximum prices you will pay for the Item, based on the available variants (SKUs).

minimum_advertised_price_range
: (object) The Minimum Advertised Price Range object contains the minimum and maximum MAPs for the item, based on the available variants (SKUs).

msrp_range
: (object) The Manufacturer's Suggested Retail Price Range object contains the minimum and maximum MSRPs for the Item, based on the available variants (SKUs).

product_images
: (array) The Product Images list stores a list of images for the item, based on the available variants (SKUs)

product_videos
: (array) The Product videos list stores a list of videos for the item, based on the available variants (SKUs)

categories
: (array) The Categories array contains objects that describe the path to the item.  It is structured like categories=[{'path': ['home', 'garden'], description: 'some string'}] where the item would exist in the garden category which has home as it's parent. Not implemented yet is passing in the category path description, so an empty string will currently be returned for description.

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

#### Supplier Object:

{% include timp/product/response/supplier_minimal.md %}

#### Cost Range Object:

{% include timp/product/response/cost_range.md %}

#### Minimum Advertized Price Range Object:

{% include timp/product/response/map_range.md %}

#### Manufacturer's Suggested Retail Price (MSRP) Range Object:

{% include timp/product/response/msrp_range.md %}

#### Product Images Object:

{% include timp/product/response/image.md %}

#### Product Videos Object:

{% include timp/product/response/video.md %}

#### Custom Attributes Object

{% include timp/objects/attributes.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/timp/products/items/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "description": "This is the default description. In this description the product is explained in detail. The idea with the description is to include everything that isn'"'"'t already included elsewhere in the item attributes, such as manufacturer, brand, country_of_origin, shipping_origin_country, marketplace_restrictions, fba_certified, etc.",
  "categories": [
    {
      "path": [
        "computer",
        "games"
      ]
    }
  ],
  "shipping_origin_country": "US",
  "country_of_origin": "CN",
  "category_id": "8hVEcErHcJToqARWeITB6yvdmrXsbH6x",
  "item_id": "J2b35VAXEumkduUhm5ik3MlQ6AS55UgE",
  "brand": "The Brand",
  "other_marketplace_restriction": "eBay, Amazon, Sears, Walmart",
  "fba_certified": false,
  "title": "The Item Title - GeUHLUfHYx",
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
http --json POST 'https://api-sandbox.cruxconnect.com/timp/products/items/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    description="This is the default description. In this description the product is explained in detail. The idea with the description is to include everything that isn't already included elsewhere in the item attributes, such as manufacturer, brand, country_of_origin, shipping_origin_country, marketplace_restrictions, fba_certified, etc." \
    categories:="[
  {
    \"path\": [
      \"computer\",
      \"games\"
    ]
  }
]" \
    shipping_origin_country="US" \
    country_of_origin="CN" \
    category_id="8hVEcErHcJToqARWeITB6yvdmrXsbH6x" \
    item_id="J2b35VAXEumkduUhm5ik3MlQ6AS55UgE" \
    brand="The Brand" \
    other_marketplace_restriction="eBay, Amazon, Sears, Walmart" \
    fba_certified:=false \
    title="The Item Title - GeUHLUfHYx" \
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
    # Create Item
    # POST https://api-sandbox.cruxconnect.com/timp/products/items/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/timp/products/items/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    description="This is the default description. In this description the product is explained in detail. The idea with the description is to include everything that isn't already included elsewhere in the item attributes, such as manufacturer, brand, country_of_origin, shipping_origin_country, marketplace_restrictions, fba_certified, etc." \
    categories:="[
  {
    \"path\": [
      \"computer\",
      \"games\"
    ]
  }
]" \
    shipping_origin_country="US" \
    country_of_origin="CN" \
    category_id="8hVEcErHcJToqARWeITB6yvdmrXsbH6x" \
    item_id="J2b35VAXEumkduUhm5ik3MlQ6AS55UgE" \
    brand="The Brand" \
    other_marketplace_restriction="eBay, Amazon, Sears, Walmart" \
    fba_certified:=false \
    title="The Item Title - GeUHLUfHYx" \
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
// request Create Item
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/products/items/',
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
    request.write("{\"item_id\":\"J2b35VAXEumkduUhm5ik3MlQ6AS55UgE\",\"title\":\"The Item Title - GeUHLUfHYx\",\"description\":\"This is the default description. In this description the product is explained in detail. The idea with the description is to include everything that isn't already included elsewhere in the item attributes, such as manufacturer, brand, country_of_origin, shipping_origin_country, marketplace_restrictions, fba_certified, etc.\",\"warranty\":\"The warranty information is included here\",\"return_policy\":\"The return policy is included here\",\"manufacturer\":\"The Manufacturer\",\"brand\":\"The Brand\",\"country_of_origin\":\"CN\",\"shipping_origin_country\":\"US\",\"other_marketplace_restriction\":\"eBay, Amazon, Sears, Walmart\",\"fba_certified\":false,\"category_id\":\"8hVEcErHcJToqARWeITB6yvdmrXsbH6x\",\"custom_attributes\":{\"Color\":\"black\",\"Size\":\"15\\\" x 15\\\" x 18\\\"\"},\"categories\":[{\"path\":[\"computer\",\"games\"]}]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
