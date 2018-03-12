---
title: /products/items/search/
name: Search Items
position: 2.25
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
      "limit": 50
    }
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "search_term": "",
    "facets": {
      "shipping_origin_country": [
        {
          "name": "Åland Islands",
          "uuid": "AX",
          "selected": false,
          "count": 1
        },
        {
          "name": "Cameroon",
          "uuid": "CM",
          "selected": false,
          "count": 1
        },
        {
          "name": "United Kingdom of Great Britain and Northern Ireland",
          "uuid": "GB",
          "selected": false,
          "count": 1
        }
      ],
      "catalogs": [
        {
          "name": "The capital powder catalog",
          "uuid": "702c0a58-503e-4bdb-9b9e-e78065c7f120",
          "selected": false,
          "count": 3
        },
        {
          "name": "master",
          "uuid": "962900df-0bd3-447b-9bdd-caff66a14591",
          "selected": false,
          "count": 3
        },
        {
          "name": "The enthusiastic winter catalog",
          "uuid": "5d704568-d5a6-4751-94ff-cc0d86da99dc",
          "selected": false,
          "count": 2
        }
      ],
      "bundle_type": [
        {
          "name": "Case Pack",
          "uuid": "case_pack",
          "selected": false,
          "count": 6
        },
        {
          "name": "Single",
          "uuid": "single",
          "selected": false,
          "count": 6
        }
      ],
      "condition": [
        {
          "name": "Refurbished",
          "uuid": "refurb",
          "selected": false,
          "count": 5
        },
        {
          "name": "New",
          "uuid": "new",
          "selected": false,
          "count": 4
        },
        {
          "name": "Used",
          "uuid": "used",
          "selected": false,
          "count": 4
        }
      ],
      "inventory_lists": [
        {
          "name": "The enchanted act inventory list",
          "uuid": "c9b32603-f6bf-4f49-89fd-8424399974f2",
          "selected": false,
          "count": 7
        },
        {
          "name": "The aching hook inventory list",
          "uuid": "044a84c9-624f-49f1-bb31-29da46dd8aa9",
          "selected": false,
          "count": 6
        },
        {
          "name": "The empty calendar inventory list",
          "uuid": "44a1f968-1ce8-4826-9cd9-f8a54f5d542d",
          "selected": false,
          "count": 2
        }
      ],
      "categories": {
        "f2ee86d6-7384-4144-bc35-428cd8e02c16": [
          {
            "name": "abounding love l0",
            "uuid": "89cfeab6-5923-47c5-a218-616f339992f0",
            "selected": false,
            "count": 1
          }
        ],
        "ce4f9803-7870-4a78-b2cb-8949c8f550d6": [
          {
            "name": "capricious jam l0",
            "uuid": "789dc9d3-54b2-4b31-a35f-06c25b8705e7",
            "selected": false,
            "count": 1
          }
        ],
        "9ff4ca63-7a46-4eee-a4fb-859e201460c8": [
          {
            "name": "abiding peace l0",
            "uuid": "5c1b9547-54df-4d6f-96c4-3c92a9768512",
            "selected": false,
            "count": 1
          }
        ]
      },
      "shipping_cost_type": [
        {
          "name": "Fixed",
          "uuid": "fixed",
          "selected": false,
          "count": 7
        },
        {
          "name": "Free",
          "uuid": "free",
          "selected": false,
          "count": 7
        },
        {
          "name": "Variable",
          "uuid": "variable",
          "selected": false,
          "count": 5
        }
      ],
      "supplier": [
        {
          "name": "projectzuul",
          "uuid": "9ff4ca63-7a46-4eee-a4fb-859e201460c8",
          "selected": false,
          "count": 3
        },
        {
          "name": "Underwood-Chavez",
          "uuid": "ce4f9803-7870-4a78-b2cb-8949c8f550d6",
          "selected": false,
          "count": 2
        },
        {
          "name": "Flynn Ltd",
          "uuid": "f2ee86d6-7384-4144-bc35-428cd8e02c16",
          "selected": false,
          "count": 2
        }
      ],
      "product_identifiers": [
        {
          "name": "UPCA",
          "uuid": "upca",
          "selected": false,
          "count": 4
        },
        {
          "name": "GTIN14",
          "uuid": "gtin14",
          "selected": false,
          "count": 6
        },
        {
          "name": "ISBN",
          "uuid": "isbn",
          "selected": false,
          "count": 6
        },
        {
          "name": "EAN13",
          "uuid": "ean13",
          "selected": false,
          "count": 5
        },
        {
          "name": "ASIN",
          "uuid": "asin",
          "selected": false,
          "count": 6
        }
      ]
    },
    "pagination": {
      "start": 0,
      "limit": 50,
      "total_count": 7
    },
    "sort": [
      "title"
    ],
    "filters": {
      "cost_per_unit": {
        "min": "0"
      },
      "quantity_in_stock": {
        "max": null,
        "min": null
      },
      "image_height": {
        "max": null,
        "min": null
      },
      "minimum_tier_quantity": {
        "max": null,
        "min": null
      },
      "image_width": {
        "max": null,
        "min": null
      }
    },
    "items": [
      {
        "uuid": "0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017",
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
            "url": "https://api.adorable.io/avatars/80/obad21.png",
            "width": 80,
            "height": 80
          },
          {
            "uuid": "b08c80af-7b64-47e7-ab49-e77c8a5b33d7",
            "url": "https://api.adorable.io/avatars/80/obad20.png",
            "width": 80,
            "height": 80
          }
        ],
        "sku_count": 5,
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
          "diameter": 1,
          "hair-color": "black"
        },
        "categories": [
          66
        ]
      },
      {
        "uuid": "31adb57c-a40a-4a99-b3d0-3c6ccd8e8941",
        "restrict_from_marketplaces": [],
        "supplier": {
          "uuid": "f2ee86d6-7384-4144-bc35-428cd8e02c16",
          "name": "Flynn Ltd"
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
          "max": 77.26,
          "min": 36.31
        },
        "product_images": [
          {
            "uuid": "602a19a4-7ac8-480c-ab19-ee981051f742",
            "url": "https://api.adorable.io/avatars/80/obad21.png",
            "width": 80,
            "height": 80
          },
          {
            "uuid": "c69ea867-4a5f-4d6d-8e4d-7b25a4bee63a",
            "url": "https://api.adorable.io/avatars/80/obad15.png",
            "width": 80,
            "height": 80
          }
        ],
        "sku_count": 6,
        "created": "2017-10-23T18:25:36.394934Z",
        "last_updated": "2017-10-23T18:25:36.394978Z",
        "item_id": "ulvg8F0r",
        "title": "The cautious knowledge item",
        "description": "And that's why you don't put the language inside your cautious knowledge item. It doesn't work that way. When it's all said and done, there's still cautious knowledge item. Still. Because we care about how your cautious knowledge item looks! Our cautious knowledge item comes with built-in swim for that extra cavernous flavor. Be the kind of person your mother wanted you to me. I like, it, I love it, I want some more of it. There's just something abaft about cuddling up with your own cautious knowledge item! And then there's our cautious knowledge item, which will blow off your eminent blood!! You know you want it. Be the hero. You know what's emotional about cautious knowledge item?",
        "warranty": "A abounding warranty",
        "return_policy": null,
        "manufacturer": "crayon Corp.",
        "brand": "playground brand",
        "country_of_origin": "TV",
        "shipping_origin_country": "GB",
        "other_marketplace_restriction": null,
        "fba_certified": null,
        "custom_attributes": {
          "hair-color": "blonde",
          "hardness": 13
        },
        "categories": [
          54
        ]
      }
    ]
  }
  ~~~
  {: title="Response" }

---
Search for Items in the catalogs available to your organization using a number of filters, facets, and other helpful tools.

URL Endpoint: /products/items/search/

### Request Parameters:

filters
: (object) The Filters object parameter includes all of the potential filters you wish to include in your Search. These filters include "cost_per_unit", "number_of_item_images", "image_height", "image_width", etc.

facets
: (object) The Facets object parameter includes all of the potential facets you wish to include in your Search. These facets include "supplier", "shipping_cost_type", "shipping_origin_country", "country_of_origin", "bundle_type", "product_identifiers", "categories", etc.

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
: (list) The Inventory Lists list is a list of the inventory lists in which the SKUs resize

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
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/items/search/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
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
    "limit": 50
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
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
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
  \"limit\": 50
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
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
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
  \"limit\": 50
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
    request.write("{\"filters\":{\"cost_per_unit\":{\"min\":null,\"max\":null},\"number_of_item_images\":{\"min\":5},\"image_height\":{\"min\":0},\"image_width\":{\"min\":0}},\"facets\":{\"supplier\":[],\"shipping_cost_type\":[],\"shipping_origin_country\":[],\"bundle_type\":[],\"product_identifiers\":[],\"categories\":[]},\"search_term\":\"\",\"sort\":\"title\",\"pagination\":{\"start\":0,\"limit\":50}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
