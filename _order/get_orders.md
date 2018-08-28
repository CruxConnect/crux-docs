---
title: /timp/orders/
name: Get Orders
position: 4.00
visibility: public
method: post
description: Get the Orders for your organization
right_code: |
  ~~~ json
  {
    "start": 0,
    "limit": 1
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "total_results": 142,
    "orders": [
      {
        "uuid": "319bba9f-71b1-4a93-8abf-67a45b8fdd5c",
        "is_allocated": false,
        "purchase_order_id": "8e5b1ccb-0221-4e26-a343-cd566bfe7419",
        "created_date": "2018-06-28T12:57:30.359784Z",
        "notes": "Eaque aut inventore itaque commodi est quas laborum.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "ebf3657c-2abb-4aff-be70-69082acc9302",
          "user": {
            "name": "owner user",
            "email": "owneruser7@projectthanos.com"
          }
        },
        "address": {
          "name": "Megan King",
          "business_name": "Black-Rice",
          "address1": "08712 Villarreal Cliffs\nBishopchester, OK 45032",
          "address2": "9652 Richard Plains\nErikamouth, MP 22422-9361",
          "city": "Franklinbury",
          "state": "North Dakota",
          "postal_code": "85254",
          "phone_number": null,
          "country": "USA"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "b84ccd3c-88f8-4050-accf-e049163052e3",
            "status": "Unallocated",
            "item_uuid": "2aeabb83-938a-4d15-a48a-da84fca11d0e",
            "item_name": "The elementary seed item",
            "sku_uuid": "a7f2cdb3-f84f-463d-91dd-51de21b119b4",
            "sku_id": "q7FSuuTXgawxPxzDs3r",
            "sku_name": "The elementary seed item",
            "unit_ship_cost": 1.99,
            "sku_title_variants": null,
            "line_item_special_instructions": null,
            "cost": 0,
            "supplier_uuid": "fddc07e7-4383-4e63-929f-f10c3b0864f0",
            "supplier_name": "projectzuul",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 5,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "reject_reason": null,
              "backorder_date": null
            },
            "line_item_designation": []
          },
        ]
      }
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

### Expected Response Codes

# Short Description
Get the Orders for your organization

# Long Description
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
  "start": 0,
  "limit": 1
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/timp/orders/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    start:=0 \
    limit:=1

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
            data=json.dumps(    start:=0 \
    limit:=1)
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
    request.write("{\"start\":0,\"limit\":1}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
