---
title: /timp/orders/
name: Get Orders
position: 4.0
visibility: public
method: post
description: Get the Orders for your organization
right_code: |
  ~~~ json
  {
    "start": 0,
    "limit": 24,
    "line_item_allocation_statuses": [
      "Unallocated",
      "Allocated",
      "Partial"
    ],
    "line_item_designation": "HasTracking",
    "start_date": "2017-07-31T06:00:00.000Z",
    "end_date": "2018-08-03T06:00:00.000Z",
    "search_term": "",
    "org_uuids": [],
    "sort": {
      "key": "date",
      "value": "desc"
    }
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "total_results": 102,
    "orders": [
      {
        "uuid": "310f7b60-8c80-42d8-a3aa-780363f969c7",
        "is_allocated": false,
        "purchase_order_id": "po-bvteP3Sg",
        "created_date": "2018-04-20T22:21:04.640348Z",
        "notes": "here are some notes",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Retail Me",
          "uuid": "359204cc-c2d9-4827-b739-64c335f9fbd1",
          "user": {
            "name": " ",
            "email": "me@retailer.com"
          }
        },
        "address": {
          "name": "Bob Iger",
          "business_name": "NBC",
          "address1": "30 Rockefeller Plaza",
          "address2": "STE 123",
          "city": "New York",
          "state": "NY",
          "postal_code": "10112",
          "phone_number": "801-555-1212",
          "country": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground",
        },
        "line_items": [
          {
            "uuid": "4883055e-f7c6-4d60-b8d3-787073b1898c",
            "status": "Unallocated",
            "item_uuid": "5a5fe856-a4bd-4dd2-ac5e-e3c9c29e5ed4",
            "item_name": "The insistent room item",
            "sku_uuid": "43113405-4964-4086-b5cc-9beea7cb127e",
            "sku_id": "bK0bi12ATMo",
            "sku_name": "The insistent room item",
            "sku_title_variants": "The insistent room item {'size': 9, 'color': 'azure'}",
            "line_item_special_instructions": null,
            "cost": 18.12,
            "supplier_uuid": "e4ba749a-f899-4a03-a759-4610deb4b5ba",
            "supplier_name": "Morales, Martin and Bautista",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 18,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
    ]
  }
  ~~~
  {: title="Response" }

---
Get Orders matching certain criteria for your organization. This may contain any or all of your orders: completed, incomplete, processing, etc.


### Request Parameters:

#### Optional:

start
: (int) The Start is the number of which "Order" you would like to start. If no other filters are used, the default order, which is date created, is used. The default Start value is 0. If this filter is not included in your request, the default value is used.

limit
: (int) The Limit is the element number of "Order" in your Orders List where you would like your results to end. If you have 10 orders and you limit at 8 and start at 4, only orders 4, 5, 6, 7, and 8 are included in the results.

sort
: (object) The Sort object contains a Key to sort on and a Direction (dir) to sort in.

line_item_allocation_statuses
: (array) One or more line item statuses. Possible choices include: `Unallocated`, `Partial`, or `Allocated`

line_item_designation
: (string) Line item status designation.  One of the following : `HasTracking`, `NeedsTracking`, `Backordered`, `Rejected`, `Cancelled`

start_date
: (string) The Start Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

end_date
: (string) The End Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

term
: (string) Term can be Order UUID, PO Number or SKU ID

org_uuids
: (array) An array of Organization Universal Unique Identifiers

##### Sort Object:

{% include timp/objects/sort.md %}

### Response Parameters:

total_results
: (number) The Total Results are the total order count per your oganization

orders
: (array) An array of order objects

#### Order Object:

{% include timp/orders/response/orders.md %}

#### Fees Object:

{% include timp/objects/fees.md %}

#### Retailer Object:

name
: (string) The Organization Name within your Retailer account

uuid
: (string) The Universal Unique Identifier for your Organization

user
: (object) The User object contains your name and email address; the name and email address of the user who submitted the Create Order API call.

#### Address Object:

{% include timp/objects/address_business.md %}

#### Requested Shipping Object:

{% include timp/orders/response/requested_shipping.md %}

#### Line Item Object:

{% include timp/objects/line_item.md %}

#### Tracking Numbers Object:

{% include timp/objects/tracking_number.md %}

#### Allocation Object:

{% include timp/objects/allocation.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/timp/orders/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "org_uuids": [],
  "sort": {
    "key": "date",
    "value": "desc"
  },
  "start": 0,
  "start_date": "2017-07-31T06:00:00.000Z",
  "limit": 24,
  "line_item_designation": "HasTracking",
  "line_item_allocation_statuses": [
    "Unallocated",
    "Allocated",
    "Partial"
  ],
  "end_date": "2018-08-03T06:00:00.000Z",
  "search_term": ""
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/timp/orders/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    org_uuids:="[]" \
    sort:="{
  \"key\": \"date\",
  \"value\": \"desc\"
}" \
    start:=0 \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=24 \
    line_item_designation:="HasTracking" \
    line_item_allocation_statuses:="[
  \"Unallocated\",
  \"Allocated\",
  \"Partial\"
]" \
    end_date="2018-08-03T06:00:00.000Z" \
    search_term=""

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Orders
    # POST https://api-sandbox.cruxconnect.com/timp/orders/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/timp/orders/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    org_uuids:="[]" \
    sort:="{
  \"key\": \"date\",
  \"value\": \"desc\"
}" \
    start:=0 \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=24 \
    line_item_designation:="HasTracking" \
    line_item_allocation_statuses:="[
  \"Unallocated\",
  \"Allocated\",
  \"Partial\"
]" \
    end_date="2018-08-03T06:00:00.000Z" \
    search_term="")
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
// request Get Orders
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/orders/',
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
    request.write("{\"start\":0,\"limit\":24,\"line_item_allocation_statuses\":[\"Unallocated\",\"Allocated\",\"Partial\"],\"line_item_designation\":\"HasTracking\",\"start_date\":\"2017-07-31T06:00:00.000Z\",\"end_date\":\"2018-08-03T06:00:00.000Z\",\"search_term\":\"\",\"org_uuids\":[],\"sort\":{\"key\":\"date\",\"value\":\"desc\"}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
