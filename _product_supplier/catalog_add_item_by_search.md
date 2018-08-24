---
title: /products/catalogs/&ltcatalog_uuid&gt/add-items-by-search/
name: Catalog Add Item by Search
position: 12.02
visibility: public
method: post
description: Add Items to an existing Catalog by Search
right_code: |
  ~~~ json
  {
    "filters": {
      "cost_per_unit": {
        "min": "0"
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


---
Add Items to an existing Catalog by Search. This allows you to add Items with all associated SKUs via a Search to a Catalog. By providing your catalog_uuid and search criteria, you can successfully add them to the indicated Catalog.

### URL Parameters:

catalog-uuid
: (string) Unique Universal Identifier for the Catalog

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

{% include timp/product/filters.md %}

#### Facets Object:

{% include timp/product/facets.md %}

#### Pagination Object:

{% include timp/product/request/pagination.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/products/catalogs/e689e8ca-79f6-4533-b12f-1c528e2aa5cd/add-items-by-search/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "search_term": "",
  "filters": {
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
http --json POST 'https://api-sandbox.cruxconnect.com/products/catalogs/e689e8ca-79f6-4533-b12f-1c528e2aa5cd/add-items-by-search/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    search_term="" \
    filters:="{
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
    # Catalog Add Item by Search
    # POST https://api-sandbox.cruxconnect.com/products/catalogs/e689e8ca-79f6-4533-b12f-1c528e2aa5cd/add-items-by-search/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/products/catalogs/e689e8ca-79f6-4533-b12f-1c528e2aa5cd/add-items-by-search/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    search_term="" \
    filters:="{
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
// request Catalog Add Item by Search
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/catalogs/e689e8ca-79f6-4533-b12f-1c528e2aa5cd/add-items-by-search/',
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
    request.write("{\"filters\":{\"cost_per_unit\":{\"min\":\"0\"}},\"facets\":{\"supplier\":[],\"shipping_cost_type\":[],\"shipping_origin_country\":[],\"bundle_type\":[],\"product_identifiers\":[],\"categories\":[]},\"search_term\":\"\",\"sort\":\"title\",\"pagination\":{\"start\":0,\"limit\":50}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
