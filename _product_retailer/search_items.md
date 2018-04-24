---
title: /products/items/search/
name: Search Items
position: 2.25
visibility: public
method: post
description: Search for Items in the catalogs available to your organization
right_code: |
  ~~~ json
  {
    "filters": {
      "cost_per_unit": {
        "min": null,
        "max": null
      },
      "number_of_item_images": {
        "min": 5
      },
      "image_height": {
        "min": 0
      },
      "image_width": {
        "min": 0
      }
    },
    "facets": {
      "supplier": [],
      "shipping_cost_type": [],
      "shipping_origin_country": [],
      "bundle_type": [],
      "product_identifiers": [],
      "categories": []
    },
    "search_term": "",
    "sort": "title",
    "pagination": {
      "start": 0,
      "limit": 1
    }
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "sort": [
      "title"
    ],
    "items": [
      {
        "uuid": "925113ca-ce78-4b74-acc1-9a69063f78f2",
        "restrict_from_marketplaces": [],
        "supplier": {
          "uuid": "86ab12cd-fd66-4122-8b81-f837bc72d755",
          "name": "Morales, Martin and Bautista"
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
          "max": 176.32,
          "min": 35.55
        },
        "product_images": [
          {
            "uuid": "a8f55104-b70e-4740-bf9b-e366c938544c",
            "url": "https://picsum.photos/80/?image=5",
            "width": 80,
            "height": 80
          },
          {
            "uuid": "fe5557a9-e09e-427f-9476-881be31fa175",
            "url": "https://picsum.photos/285/?image=29",
            "width": 285,
            "height": 285
          }
        ],
        "sku_count": 10,
        "created": "2018-04-06T01:12:10.568241Z",
        "last_updated": "2018-04-06T01:12:10.568302Z",
        "item_id": "E6eRLoSjJP",
        "title": "The chunky boot item",
        "description": "Our chunky boot item comes with built-in kitty for that extra chemical flavor. You know you want it.",
        "warranty": "A edible warranty",
        "return_policy": null,
        "manufacturer": "waste Corp.",
        "brand": "thought brand",
        "country_of_origin": "JO",
        "shipping_origin_country": "BV",
        "other_marketplace_restriction": null,
        "fba_certified": null,
        "custom_attributes": {
          "hardness": 19,
          "diameter": 9
        },
        "categories": [
          {
            "uuid": "3aca44e5-17d1-4510-84d1-72c2eb8c1357",
            "path": [
              "candid grass l0"
            ],
            "description": ""
          }
        ]
      }
    ],
    "facets": {
      "catalogs": [
        {
          "name": "The elfin industry catalog",
          "count": 5,
          "uuid": "38504ca3-27ea-4478-85a2-25f01cde1652",
          "selected": false
        }
      ],
      "supplier": [
        {
          "name": "Morales, Martin and Bautista",
          "count": 5,
          "uuid": "e4ba749a-f899-4a03-a759-4610deb4b5ba",
          "selected": false
        }
      ],
      "catalog_type": [
        "standard"
      ],
      "shipping_origin_country": [
        {
          "name": "Argentina",
          "count": 1,
          "uuid": "AR",
          "selected": false
        },
        {
          "name": "Åland Islands",
          "count": 1,
          "uuid": "AX",
          "selected": false
        },
        {
          "name": "Bulgaria",
          "count": 1,
          "uuid": "BG",
          "selected": false
        },
        {
          "name": "Bouvet Island",
          "count": 1,
          "uuid": "BV",
          "selected": false
        },
        {
          "name": "Tanzania, United Republic of",
          "count": 1,
          "uuid": "TZ",
          "selected": false
        }
      ],
      "categories": {
        "e4ba749a-f899-4a03-a759-4610deb4b5ba": [
          {
            "name": "candid grass l0",
            "count": 3,
            "uuid": "3aca44e5-17d1-4510-84d1-72c2eb8c1357",
            "selected": false
          }
        ]
      },
      "condition": [
        {
          "name": "Used",
          "count": 5,
          "uuid": "used",
          "selected": false
        },
        {
          "name": "New",
          "count": 4,
          "uuid": "new",
          "selected": false
        },
        {
          "name": "Refurbished",
          "count": 4,
          "uuid": "refurb",
          "selected": false
        }
      ],
      "inventory_lists": [
        {
          "name": "The absurd ear inventory list",
          "count": 5,
          "uuid": "1431483d-f893-45a4-8a73-0a46c44d15c5",
          "selected": false
        },
        {
          "name": "The ablaze duck inventory list",
          "count": 5,
          "uuid": "5d173491-52ad-4650-91cf-b279475f978d",
          "selected": false
        }
      ],
      "shipping_cost_type": [
        {
          "name": "Fixed",
          "count": 5,
          "uuid": "fixed",
          "selected": false
        },
        {
          "name": "Free",
          "count": 5,
          "uuid": "free",
          "selected": false
        },
        {
          "name": "Variable",
          "count": 5,
          "uuid": "variable",
          "selected": false
        }
      ],
      "product_identifiers": [],
      "bundle_type": [
        {
          "name": "Case Pack",
          "count": 5,
          "uuid": "case_pack",
          "selected": false
        },
        {
          "name": "Single",
          "count": 3,
          "uuid": "single",
          "selected": false
        }
      ]
    },
    "filters": {
      "minimum_tier_quantity": {
        "max": null,
        "min": null
      },
      "image_height": {
        "min": 0
      },
      "image_width": {
        "min": 0
      },
      "number_of_item_images": {
        "min": 5
      },
      "quantity_in_stock": {
        "max": null,
        "min": null
      },
      "cost_per_unit": {
        "max": null,
        "min": null
      }
    },
    "search_term": "",
    "pagination": {
      "start": 0,
      "total_count": 5,
      "limit": 1
    }
  }
  ~~~
  {: title="Response" }

---
Search for Items in the catalogs available to your organization using a number of filters, facets, and other helpful tools.


### Request Parameters:

filters
: (object) The Filters object parameter includes all of the potential filters you wish to include in your Search. These filters include "cost_per_unit", "number_of_item_images", "image_height", "image_width", etc.

facets
: (object) The Facets object parameter includes all of the potential facets you wish to include in your Search. These facets include "supplier", "shipping_cost_type", "shipping_origin_country", "country_of_origin", "bundle_type", "product_identifiers", "categories", catalog_type, etc.

search_term
: (string) The Search Term you would like to search for

sort
: (string) The Sort parameter indicates what attribute on which you would like to sort

pagination
: (object) The Pagination object includes start and limit which allow you to receive a manageable amount of data back from your API call.

#### Filters Object:

cost_per_unit
: (object) The Cost Per Unit object may contain a minimum and a maximum number

number_of_item_images
: (object) The Number of Item Images object may contain a minimum and a maximum number

image_height
: (object) The Image Height object may contain a minimum and a maximum number

image_width
: (object) The Image Width object may contain a minimum and a maximum number

#### Facets Object:

supplier
: (list) The Supplier list is a list of suppliers using uuid or name

shipping_cost_type
: (list) The Shipping Cost Type list is a list of types of shipping costs the Supplier has set up

shipping_origin_country
: (list) The Shipping Origin Country list is a list of countries using the country codes. Values include "US", "CA", "MX", etc.

bundle_type
: (list) The Bundle Type list is a list of bundle types the Supplier has set up for the SKUs. Values for bundle_type_name include "Case Pack" and "Single".

product_identifiers
: (list) The Product Identifiers list is a list of product identifiers available on each SKU

categories
: (list) The Categories list is a list of categories in which SKUs may reside

#### Pagination Object:

start
: (number) The Start parameter indicates on which element of the list of results the pagination should begin.

limit
: (number) The Limit parameter indicates one which element of the list of results the pagination should end.

### Response Parameters:

pagination
: (object) The Pagination object parameter includes the total_count, start, and limit for your Search.

items
: (list) The Items list is a list of Items that match the criteria you provided for your Search.

search_term
: (string) The Search Term used to filter the results of your Search

sort
: (list) The Sort list parameter includes the attribute(s) on which you are performing a Sort on your Search

facets
: (object) The Facets object contains product_identifiers, bundle_type, condition, supplier, catalogs, categories, shipping_origin_country, shipping_cost_type, and inventory lists

filters
: (object) The Filters object contains image_width, cost_per_unit, minimum_tier_quantity, quantity_in_stock, and image_height

#### Pagination Object:

total_count
: (number) The Total Count of results returned for this Search

start
: (number) The Start parameter indicates on which element of the list of results the pagination should begin.

limit
: (number) The Limit parameter indicates one which element of the list of results the pagination should end.

#### Item Object:

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
: (list) The list of Price Tier objects on this SKU

product_images
: (list) The Product Images are a list of product image objects for the SKU which contain a uuid, url, width, and height of the image.

measurements
: (object) The Measurements object contains sku measurements object and a package measurements object.

product_identifiers
: (object) The Product Identifiers object contains the upca, ean13, gtin14, isbn, asin, and mpn for the SKU.

inventory_lists
: (list) The Inventory lists list contains all of the Inventory list objects where this SKU currently resides.

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
: (string) The units utilized by the supplier for weight ('g', 'kg', 'lb', and 'oz' are potential options)

length
: (number) The Length of the SKU in "dimension_units"

width
: (number) The Width of the SKU in "dimension_units"

height
: (number) The Height of the SKU in "dimension_units"

dimension_units
: (string) The units utilized by the supplier for dimensions ('cm', 'm', 'in', and 'ft' are potential options)

#### Package Measurements Object:

weight
: (number) The Weight of the packaged SKU in the "weight_units"

weight_units
: (string) The units utilized by the supplier for weight ('g', 'kg', 'lb', and 'oz' are potential options)

length
: (number) The Length of the packaged SKU in "dimension_units"

width
: (number) The Width of the packaged SKU in "dimension_units"

height
: (number) The Height of the packaged SKU in "dimension_units"

dimension_units
: (string) The units utilized by the supplier for dimensions ('cm', 'm', 'in', and 'ft' are potential options)

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

#### Inventory list Object:

uuid
: (string) The Universal Unique Identifier for the Inventory list

name
: (string) The Name your company has given to this Inventory list

Supplier Object:

uuid
: (string) The Universal Unique Identifier for the Supplier

name
: (string) The Supplier Name

#### Cost Range Object:

min
: (number) The Minimum price for one of the SKUs or Item-variants

max
: (number) The Maximum price for one of the SKUs or Item-variants

Minimum Advertized Price Range Object:

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

#### Facets Object:

product_identifiers
: (list) The Product Identifiers list is a list of product identifiers available on each SKU

bundle_type
: (list) The Bundle Type list is a list of bundle types the Supplier has set up for the SKUs. Values for bundle_type_name include "Case Pack" and "Single".

condition
: (list) The Condition list is a list of conditions and counts for each pertaining to the Items of your results

supplier
: (list) The Supplier list is a list of suppliers using uuid or name

catalogs
: (list) The Catalogs list is a list of catalogs in which SKUs reside

categories
: (list) The Categories list is a list of categories in which SKUs reside

shipping_origin_country
: (list) The Shipping Origin Country list is a list of countries using the country codes. Values include "US", "CA", "MX", etc.

shipping_cost_type
: (list) The Shipping Cost Type list is a list of types of shipping costs the Supplier has set up

inventory_lists
: (list) The Inventory lists list is a list of the inventory lists in which the SKUs resize

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/items/search/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "search_term": "",
  "filters": {
    "image_height": {
      "min": 0
    },
    "image_width": {
      "min": 0
    },
    "number_of_item_images": {
      "min": 5
    },
    "cost_per_unit": {
      "min": null,
      "max": null
    }
  },
  "pagination": {
    "start": 0,
    "limit": 1
  },
  "sort": "title",
  "facets": {
    "supplier": [],
    "shipping_cost_type": [],
    "shipping_origin_country": [],
    "bundle_type": [],
    "product_identifiers": [],
    "categories": []
  }
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/products/items/search/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    search_term="" \
    filters:="{
  \"image_height\": {
    \"min\": 0
  },
  \"image_width\": {
    \"min\": 0
  },
  \"number_of_item_images\": {
    \"min\": 5
  },
  \"cost_per_unit\": {
    \"min\": null,
    \"max\": null
  }
}" \
    pagination:="{
  \"start\": 0,
  \"limit\": 1
}" \
    sort="title" \
    facets:="{
  \"supplier\": [],
  \"shipping_cost_type\": [],
  \"shipping_origin_country\": [],
  \"bundle_type\": [],
  \"product_identifiers\": [],
  \"categories\": []
}"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Search Items
    # POST https://api-sandbox.cruxconnect.com/products/items/search/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/items/search/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    search_term="" \
    filters:="{
  \"image_height\": {
    \"min\": 0
  },
  \"image_width\": {
    \"min\": 0
  },
  \"number_of_item_images\": {
    \"min\": 5
  },
  \"cost_per_unit\": {
    \"min\": null,
    \"max\": null
  }
}" \
    pagination:="{
  \"start\": 0,
  \"limit\": 1
}" \
    sort="title" \
    facets:="{
  \"supplier\": [],
  \"shipping_cost_type\": [],
  \"shipping_origin_country\": [],
  \"bundle_type\": [],
  \"product_identifiers\": [],
  \"categories\": []
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
// request Search Items
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/items/search/',
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
    request.write("{\"filters\":{\"cost_per_unit\":{\"min\":null,\"max\":null},\"number_of_item_images\":{\"min\":5},\"image_height\":{\"min\":0},\"image_width\":{\"min\":0}},\"facets\":{\"supplier\":[],\"shipping_cost_type\":[],\"shipping_origin_country\":[],\"bundle_type\":[],\"product_identifiers\":[],\"categories\":[]},\"search_term\":\"\",\"sort\":\"title\",\"pagination\":{\"start\":0,\"limit\":1}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
