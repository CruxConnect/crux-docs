---
title: /orders/
name: Get Orders
position: 4.00
visibility: public
method: post
description: Get the Orders for your organization
right_code: |
  ~~~ json
  {
    "start": 0,
    "limit": 1,
    "line_item_statuses": [
      "unallocated"
    ],
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
    "total_results": 108,
    "orders": [
      {
        "uuid": "49bd2a6d-fe6b-4145-a059-9439289801ae",
        "is_allocated": false,
        "purchase_order_id": "po-5fkQo2ET",
        "created_date": "2018-03-08T22:20:25.311697Z",
        "notes": "here are some notes",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Crux User",
            "email": "user@mycompany.com"
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
          "phone_number": null,
          "country": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "9af950c1-5dac-4da4-a86c-f1a0f3bdff40",
            "status": "Unallocated",
            "item_uuid": "a904832e-2ad4-4ad7-8339-e4b0877a42bd",
            "item_name": "PulseTech Xtreme Charger Auto  100X010 XC100-P",
            "sku_uuid": "f9ded77b-35b2-45e1-a071-2eec8e99f581",
            "sku_id": "000106",
            "sku_name": "PulseTech Xtreme Charger Auto  100X010 XC100-P",
            "sku_title_variants": "PulseTech Xtreme Charger Auto  100X010 XC100-P {}",
            "sku_special_instructions": null,
            "cost": 66.05,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 475,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "3b6bf17a-1a95-41c7-8961-52ac8459c986",
        "is_allocated": false,
        "purchase_order_id": "po-WbbQy4Nu",
        "created_date": "2018-02-26T15:45:17.390064Z",
        "notes": "here are some notes",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Crux User",
            "email": "user@mycompany.com"
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
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "052cae65-0332-4e8a-820a-3d482913e810",
            "status": "Unallocated",
            "item_uuid": "a904832e-2ad4-4ad7-8339-e4b0877a42bd",
            "item_name": "PulseTech Xtreme Charger Auto  100X010 XC100-P",
            "sku_uuid": "f9ded77b-35b2-45e1-a071-2eec8e99f581",
            "sku_id": "000106",
            "sku_name": "PulseTech Xtreme Charger Auto  100X010 XC100-P",
            "cost": 66.05,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 236,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
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

line_item_statuses
: (array) One or more line item statuses. Will include orders with statuses based upon that `status_conjunction`. Possible Values are: `Unallocated`, `Allocated`, `Rejected`, `HasTracking`, `Backordered`, `Cancelled`. The response will contain orders with statuses that match the provided line_item_status (as combined based on line_item_status_conjunction).

start_date
: (string) The Start Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

end_date
: (string) The End Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

term
: (string) Term can be Order UUID, PO Number or SKU ID

org_uuids
: (array) An array of Organization Universal Unique Identifiers

##### Sort Object:

{% include objects/sort.md %}

### Response Parameters:

total_results
: (number) The Total Results are the total order count per your oganization

orders
: (array) The list of orders per your organization

#### Order Object:

uuid
: (string) The Universal Unique Identifier for the Order

is_allocated
: (boolean) Is the order Allocated by the Supplier as of the moment you get the response. Generally, this is false initially as the supplier(s) providing the SKU(s) must allocate for each Order.

purchase_order_id
: (string) The Purchase Order (PO) Identifier for this order. This is the one you provided in the request parameters. It is the Identifer that your organization uses to identify the Order.

created_date
: (string) The Date when the order was created. It will always be the same day as when you send in the request to Create the Order.

notes
: (string) The notes you provided from your request to create the Order.

fees
: (object) The Fees object contains the estimated shipping cost, drop ship fee, and order fee

retailer
: (object) The Retailer object contains an organization name, organization uuid, and a user object

address
: (object) The Address object containing name, business name, address line 1, address line 2, city, state, postal code

requested_shipping
: (object) The Requested Shipping object contains the shipping carrier and shipping method from the request to create the Order.

line_items
: (array) The Line Items list contains line items with their uuid, item uuid, item name, status, sku uuid, sku id, sku name, cost, supplier uuid, supplier name, tracking numbers object, and allocation object.

#### Fees Object:

{% include objects/fees.md %}

#### Retailer Object:

name
: (string) The Organization Name within your Retailer account

uuid
: (string) The Universal Unique Identifier for your Organization

user
: (object) The User object contains your name and email address; the name and email address of the user who submitted the Create Order API call.

#### Address Object:

{% include objects/address_business.md %}

#### Requested Shipping Object:

shipping_carrier
: (string) The Shipping Carrier to deliver the order

shipping_method
: (string) The Shipping Method used by the Shipping Carrier to deliver the order

#### Line Item Object:

{% include objects/line_item.md %}

#### Tracking Numbers Object:

{% include objects/tracking_number.md %}

#### Allocation Object:

{% include objects/allocation.md %}

Expected responses include 200, 400, 401, 403, or 404.


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/orders/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "sort": {
    "key": "date",
    "value": "desc"
  },
  "start": 0,
  "start_date": "2017-07-31T06:00:00.000Z",
  "limit": 1,
  "line_item_statuses": [
    "unallocated"
  ],
  "end_date": "2018-08-03T06:00:00.000Z",
  "search_term": "",
  "org_uuids": []
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/orders/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    sort:="{
  \"key\": \"date\",
  \"value\": \"desc\"
}" \
    start:=0 \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=1 \
    line_item_statuses:="[
  \"unallocated\"
]" \
    end_date="2018-08-03T06:00:00.000Z" \
    search_term="" \
    org_uuids:="[]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Orders
    # POST https://api-sandbox.cruxconnect.com/orders/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/orders/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    sort:="{
  \"key\": \"date\",
  \"value\": \"desc\"
}" \
    start:=0 \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=1 \
    line_item_statuses:="[
  \"unallocated\"
]" \
    end_date="2018-08-03T06:00:00.000Z" \
    search_term="" \
    org_uuids:="[]")
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
        path: '/orders/',
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
    request.write("{\"start\":0,\"limit\":1,\"line_item_statuses\":[\"unallocated\"],\"start_date\":\"2017-07-31T06:00:00.000Z\",\"end_date\":\"2018-08-03T06:00:00.000Z\",\"search_term\":\"\",\"org_uuids\":[],\"sort\":{\"key\":\"date\",\"value\":\"desc\"}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
