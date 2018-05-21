---
title: /products/items/search/
name: Search Items
position: 4.05
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
            "uri_type": "url",
            "width": 80,
            "height": 80
          },
        ],
        "product_videos": [
          {
            "uuid": "84926340-b70e-4740-bf9b-e366c938544c",
            "url": "https://somewhere.videos/80/?video=3",
            "uri_type": "url",
          },
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
        ],
        "catalog_type": [],
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

##### Optional

{% include product/request/search_params.md %}

#### Filters Object:

{% include product/filters.md %}

#### Facets Object:

{% include product/facets.md %}

#### Pagination Object:

{% include product/request/pagination.md %}

### Response Parameters:

items
: (array) Array of Item Objects that match the criteria you provided for your Search.

filters
: (object) The Filters object contains image_width, cost_per_unit, minimum_tier_quantity, quantity_in_stock, and image_height

facets
: (object) The Facets object contains product_identifiers, bundle_type, condition, supplier, catalogs, categories, shipping_origin_country, shipping_cost_type, catalog_type, and inventory lists

pagination
: (object) The Pagination object parameter includes the total_count, start, and limit for your Search.

search_term
: (string) The Search Term used to filter the results of your Search

sort
: (array) The Sort list parameter includes the attribute(s) on which you are performing a Sort on your Search


#### Pagination Object:

{% include product/response/pagination.md %}

#### Item Object:

{% include product/response/item.md %}

#### SKU Object:

{% include product/response/sku.md %}

#### Price Tier Object:

{% include product/response/price_tier.md %}

#### Product Image Object:

{% include product/response/image.md %}

#### Product Video Object:

{% include product/response/video.md %}

#### SKU Measurements Object:

{% include product/response/measurements_sku.md %}

#### Package Measurements Object:

{% include product/response/measurements_package.md %}

#### Product Identifiers Object:

{% include product/response/product_identifiers.md %}

#### Inventory List Object:

{% include product/response/inventory_list_minimal.md %}

### Supplier Object:

{% include product/response/supplier_minimal.md %}

#### Cost Range Object:

{% include product/response/cost_range.md %}

### Minimum Advertized Price Range Object:

{% include product/response/map_range.md %}

#### Manufacturer's Suggested Retail Price (MSRP) Range Object:

{% include product/response/msrp_range.md %}

#### Item Product Images Object:

{% include product/response/image.md %}

#### Product Videos Object:

{% include product/response/video.md %}

#### Facets Object:

{% include product/facets.md %}

### Filters Object:

{% include product/filters.md %}

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
