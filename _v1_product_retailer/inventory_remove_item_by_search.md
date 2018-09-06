---
title: /products/inventory-lists/&lt;inventory_list_uuid&gt;/remove-items-by-search/
name: Inventory Remove Item by Search
position: 11.06
visibility: v1
method: post
description: Remove Items from an existing Inventory List by Search
right_code: |
  ~~~ json
  {
    "filters": {
      "cost_per_unit": {
        "min": "0"
      },
      "number_of_item_images": {
        "min": 0,
        "max": "500"
      },
      "image_height": {
        "min": 0,
        "max": 100000
      },
      "image_width": {
        "min": 0,
        "max": 100000
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
      "limit": 50
    }
  }
  ~~~
  {: title="Request" }


---
Remove Items with all associated SKUs based upon your search criteria to an existing Inventory List.

### URL Parameters

inventory_list_uuid
: (string) Universal Unique Identifier for the Inventory List

### Request Parameters:

filters
: (object) The Filters object parameter includes all of the potential filters you wish to include in your Search.

facets
: (object) The Facets object parameter includes all of the potential facets you wish to include in your Search.

search_term
: (string) The Search Term you would like to search for

sort
: (string) The Sort parameter indicates what attribute on which you would like to sort

pagination
: (object) The Pagination object includes start and limit which allow you to receive a manageable amount of data back from your API call.

#### Filters Object

{% include v1/product/filters.md %}

#### Facets Object

{% include v1/product/facets.md %}

#### Pagination Object
{% include v1/product/request/pagination.md %}

### Expected Response Codes

{% include v1/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/remove-items-by-search/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "search_term": "",
  "filters": {
    "image_height": {
      "min": 0,
      "max": 100000
    },
    "image_width": {
      "min": 0,
      "max": 100000
    },
    "number_of_item_images": {
      "min": 0,
      "max": "500"
    },
    "cost_per_unit": {
      "min": "0"
    }
  },
  "pagination": {
    "start": 0,
    "limit": 50
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
http --json POST 'https://api-sandbox.cruxconnect.com/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/remove-items-by-search/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    search_term="" \
    filters:="{
  \"image_height\": {
    \"min\": 0,
    \"max\": 100000
  },
  \"image_width\": {
    \"min\": 0,
    \"max\": 100000
  },
  \"number_of_item_images\": {
    \"min\": 0,
    \"max\": \"500\"
  },
  \"cost_per_unit\": {
    \"min\": \"0\"
  }
}" \
    pagination:="{
  \"start\": 0,
  \"limit\": 50
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
    # Inventory Remove Item by Search
    # POST https://api-sandbox.cruxconnect.com/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/remove-items-by-search/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/remove-items-by-search/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    search_term="" \
    filters:="{
  \"image_height\": {
    \"min\": 0,
    \"max\": 100000
  },
  \"image_width\": {
    \"min\": 0,
    \"max\": 100000
  },
  \"number_of_item_images\": {
    \"min\": 0,
    \"max\": \"500\"
  },
  \"cost_per_unit\": {
    \"min\": \"0\"
  }
}" \
    pagination:="{
  \"start\": 0,
  \"limit\": 50
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
// request Inventory Remove Item by Search
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/inventory-lists/054c051c-891d-4063-a299-62d6e5036e53/remove-items-by-search/',
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
    request.write("{\"filters\":{\"cost_per_unit\":{\"min\":\"0\"},\"number_of_item_images\":{\"min\":0,\"max\":\"500\"},\"image_height\":{\"min\":0,\"max\":100000},\"image_width\":{\"min\":0,\"max\":100000}},\"facets\":{\"supplier\":[],\"shipping_cost_type\":[],\"shipping_origin_country\":[],\"bundle_type\":[],\"product_identifiers\":[],\"categories\":[],\"catalog_type\":[]},\"search_term\":\"\",\"sort\":\"title\",\"pagination\":{\"start\":0,\"limit\":50}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
