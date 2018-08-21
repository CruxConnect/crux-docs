---
title: /timp/products/items/search/
name: Search Items
position: 2.05
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
      "categories": [],
      "catalog_type": []
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
    "pagination": {
      "start": 0,
      "limit": 1,
      "total_count": 0
    },
    "items": [],
    "facets": {
      "product_identifiers": [],
      "bundle_type": [],
      "catalog_type": [
        "standard"
      ],
      "catalogs": [],
      "categories": {},
      "condition": [],
      "inventory_lists": [],
      "shipping_cost_type": [],
      "shipping_origin_country": [],
      "supplier": []
    },
    "sort": [
      "title"
    ],
    "search_term": "",
    "filters": {
      "cost_per_unit": {
        "min": null,
        "max": null
      },
      "minimum_tier_quantity": {
        "min": null,
        "max": null
      },
      "quantity_in_stock": {
        "min": null,
        "max": null
      },
      "image_height": {
        "min": 0
      },
      "image_width": {
        "min": 0
      },
      "number_of_item_images": {
        "min": 5
      }
    }
  }
  ~~~
  {: title="Response" }

---
Search for Items in the catalogs available to your organization using a number of filters, facets, and other helpful tools.


### Request Parameters:

##### Optional

{% include timp/product/request/search_params.md %}

#### Filters Object:

{% include timp/product/filters.md %}

#### Facets Object:

{% include timp/product/facets.md %}

#### Pagination Object:

{% include timp/product/request/pagination.md %}

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

{% include timp/product/response/pagination.md %}

#### Item Object:

{% include timp/product/response/item.md %}

#### SKU Object:

{% include timp/product/response/sku.md %}

#### Price Tier Object:

{% include timp/product/response/price_tier.md %}

#### Product Image Object:

{% include timp/product/response/image.md %}

#### Product Video Object:

{% include timp/product/response/video.md %}

#### SKU Measurements Object:

{% include timp/product/response/measurements_sku.md %}

#### Package Measurements Object:

{% include timp/product/response/measurements_package.md %}

#### Product Identifiers Object:

{% include timp/product/response/product_identifiers.md %}

#### Inventory List Object:

{% include timp/product/response/inventory_list_minimal.md %}

### Supplier Object:

{% include timp/product/response/supplier_minimal.md %}

#### Cost Range Object:

{% include timp/product/response/cost_range.md %}

### Minimum Advertized Price Range Object:

{% include timp/product/response/map_range.md %}

#### Manufacturer's Suggested Retail Price (MSRP) Range Object:

{% include timp/product/response/msrp_range.md %}

#### Item Product Images Object:

{% include timp/product/response/image.md %}

#### Product Videos Object:

{% include timp/product/response/video.md %}

#### Facets Object:

{% include timp/product/facets.md %}

### Filters Object:

{% include timp/product/filters.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}

### Expected Response Codes

# Short Description
Search for Items in the catalogs available to your organization

# Long Description
Search for Items in the catalogs available to your organization using a number of filters, facets, and other helpful tools.


### Request Parameters:

##### Optional

{% include timp/product/request/search_params.md %}

#### Filters Object:

{% include timp/product/filters.md %}

#### Facets Object:

{% include timp/product/facets.md %}

#### Pagination Object:

{% include timp/product/request/pagination.md %}

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

{% include timp/product/response/pagination.md %}

#### Item Object:

{% include timp/product/response/item.md %}

#### SKU Object:

{% include timp/product/response/sku.md %}

#### Price Tier Object:

{% include timp/product/response/price_tier.md %}

#### Product Image Object:

{% include timp/product/response/image.md %}

#### Product Video Object:

{% include timp/product/response/video.md %}

#### SKU Measurements Object:

{% include timp/product/response/measurements_sku.md %}

#### Package Measurements Object:

{% include timp/product/response/measurements_package.md %}

#### Product Identifiers Object:

{% include timp/product/response/product_identifiers.md %}

#### Inventory List Object:

{% include timp/product/response/inventory_list_minimal.md %}

### Supplier Object:

{% include timp/product/response/supplier_minimal.md %}

#### Cost Range Object:

{% include timp/product/response/cost_range.md %}

### Minimum Advertized Price Range Object:

{% include timp/product/response/map_range.md %}

#### Manufacturer's Suggested Retail Price (MSRP) Range Object:

{% include timp/product/response/msrp_range.md %}

#### Item Product Images Object:

{% include timp/product/response/image.md %}

#### Product Videos Object:

{% include timp/product/response/video.md %}

#### Facets Object:

{% include timp/product/facets.md %}

### Filters Object:

{% include timp/product/filters.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/timp/products/items/search/" \
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
    "shipping_origin_country": [],
    "categories": [],
    "product_identifiers": [],
    "shipping_cost_type": [],
    "catalog_type": [],
    "bundle_type": []
  }
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/timp/products/items/search/' \
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
  \"shipping_origin_country\": [],
  \"categories\": [],
  \"product_identifiers\": [],
  \"shipping_cost_type\": [],
  \"catalog_type\": [],
  \"bundle_type\": []
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
    # POST https://api-sandbox.cruxconnect.com/timp/products/items/search/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/timp/products/items/search/",
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
  \"shipping_origin_country\": [],
  \"categories\": [],
  \"product_identifiers\": [],
  \"shipping_cost_type\": [],
  \"catalog_type\": [],
  \"bundle_type\": []
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
        path: '/timp/products/items/search/',
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
    request.write("{\"filters\":{\"cost_per_unit\":{\"min\":null,\"max\":null},\"number_of_item_images\":{\"min\":5},\"image_height\":{\"min\":0},\"image_width\":{\"min\":0}},\"facets\":{\"supplier\":[],\"shipping_cost_type\":[],\"shipping_origin_country\":[],\"bundle_type\":[],\"product_identifiers\":[],\"categories\":[],\"catalog_type\":[]},\"search_term\":\"\",\"sort\":\"title\",\"pagination\":{\"start\":0,\"limit\":1}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
