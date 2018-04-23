---
title: /discovery/suppliers/
name: Discovery Supplier List
position: 3.00
visibility: public
method: post
description: A list of all suppliers available to you in the discovery catalog
right_code: |
  ~~~ json
  {
    "initial_character": "T",
    "recent": 90,
    "pagination": {
      "start": 0,
      "limit": 25
    },
    "sort": {
      "key": "number_of_skus",
      "dir": "desc"
    }
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "suppliers": [
      {
        "uuid": "b0f9550d-c180-46ca-acda-2f081feb1a46",
        "name": "Thomas-Perkins",
        "website": "romero.com",
        "description": null,
        "fulfillment_percentage": 0,
        "number_of_skus": 5,
        "contact": {
          "uuid": "ace86572-ee12-4829-9079-3e69a997e42f",
          "first_name": "owner",
          "last_name": "user",
          "email": "owneruser1@romero.com",
          "phone": "1-541-219-3109x433",
          "job_title": "Account Manager"
        }
      }
    ],
    "pagination": {
      "total_count": 1,
      "start": null,
      "limit": null
    }
  }
  ~~~
  {: title="Response" }

---
A list of all suppliers available to you in the discovery catalog

### Request Parameters:

#### Required:
none

#### Optional:

initial_character
: (string) First character of supplier name OR '#'. If a letter or number, only suppliers whose name starts with this character will be returned. If '#', suppliers whose name starts with any number (0-9) will be returned. Only the first character of the string will be considered. Letters and numbers must be from UTF-8 ranges 0030-0039 (0-9), 0041-005A (A-Z), or 0061-007A (a-z). Upper- and lower-case letters are treated the same. (Some suppliers have company names with characters not in the specified ranges, but when they join Crux they provide a simplified, standardized name that uses only the limited character set above. It is the simplified/standardized name that determines where a supplier appears in the initial_character search.)

limit
: (int) Number of suppliers displayed on a page; used for paginating results. Default: 50. Maximum: 100. Any 'limit' greater than the Maximum will be forced to the Maximum.

recent
: (int) Number of days. If specified, returns suppliers that have made their products available in the Discovery Catalog in the past 'recent' days.

sort
: (object) Field and order for sorting.

start
: (int) Element number of the first supplier that will be displayed on a page. (The available suppliers are returned in an ordered list, numbered from 0 to Number-of-suppliers, with each supplier an element in the list.) Used for paginating results. Default: 0. If greater than or equal to the number of available suppliers, 'start' is forced to the Number-of-suppliers (which will yield zero results).

{% include objects/sort.md %}

### Response Parameters:

suppliers
: (object) A list of Discovery Supplier objects (see blow)

pagination
: (object) The Pagination object parameter includes the total_count, start, and limit for your Search.

#### Suppliers

uuid
: (string) Universal Unique Identifier for the supplier

name
: (string) Supplier name. Character case is specified, eg, "McCord Manufacturing" rather than "MCCORD MANUFACTURING". Maximum length is 200 characters. Characters must be from UTF-8 ranges 0030-0039 (0-9), 0041-005A (A-Z), or 0061-007A (a-z).

contact
: (object) See below. An individual employee of the supplier designated as the contact person for Crux-related questions.

description
: (string) Summary, provided by the supplier, of what the supplier offers. The length is unconstrained.

fulfillment_percentage
: (float) Percentage of SKUs ordered from the supplier through Crux that the supplier has delivered. The fulfillment_percentage will be calculated to at least two decimal places.

number_of_skus
: (int) Number of SKUs that the supplier has made visible in the Discovery Catalog.

shipping_origin_country_name
: (string) English name of country from which SKUs are shipped. The names come from the 'Country name' column of ISO 3166-1 alpha-2 without any change in capitalization. (Note: behind the scenes, Crux only identifies a country by its two-character ISO 3166-1 alpha-2 code. If there is ever a discrepancy between the country code and the country name, the code takes precedence.)

website
: (string) Browser-ready URL for supplier's public-facing website. A URL is 'browser-ready' if we can put it in an internet browser and the website loads. (For some websites that means that the protocol needs to be specified, eg, 'https://www.awesome.com'; for others, the protocol is not required, eg, 'www.verycool.com'.)

contact
: (object)  A Contact Object

#### Contact Object

{% include objects/contact.md %}

{% include objects/response_pagination.md %}

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/discovery/suppliers/" \
     -H 'Cookie: sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp' \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "recent": 90,
  "pagination": {
    "start": 0,
    "limit": 25
  },
  "initial_character": "T",
  "sort": {
    "key": "number_of_skus",
    "dir": "desc"
  }
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/discovery/suppliers/' \
    'Cookie':'sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    recent:=90 \
    pagination:="{
  \"start\": 0,
  \"limit\": 25
}" \
    initial_character="T" \
    sort:="{
  \"key\": \"number_of_skus\",
  \"dir\": \"desc\"
}"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Discovery Supplier List
    # POST https://api-sandbox.cruxconnect.com/discovery/suppliers/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/discovery/suppliers/",
            headers={
                "Cookie": "sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp",
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    recent:=90 \
    pagination:="{
  \"start\": 0,
  \"limit\": 25
}" \
    initial_character="T" \
    sort:="{
  \"key\": \"number_of_skus\",
  \"dir\": \"desc\"
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
// request Discovery Supplier List
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/discovery/suppliers/',
        method: 'POST',
        headers: {"Cookie":"sessionid=fi1us4q9rlphkjbscpo0dtz9iltj7ovp","Authorization":"Token 1234567890","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"initial_character\":\"T\",\"recent\":90,\"pagination\":{\"start\":0,\"limit\":25},\"sort\":{\"key\":\"number_of_skus\",\"dir\":\"desc\"}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
