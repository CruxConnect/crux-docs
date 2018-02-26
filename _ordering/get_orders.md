---
title: /orders/
name: Get Orders
position: 3.00
method: post
description: Get the Orders for your organization
right_code: |
  ~~~ json
  {
    "start": 0,
    "limit": 2,
    "line_item_statuses": [
      "Unallocated"
    ],
    "line_item_status_conjunction": "or",
    "start_date": "2017-07-31T06:00:00.000Z",
    "end_date": "2018-08-03T06:00:00.000Z",
    "term": "",
    "org_uuids": [],
    "sort": {
      "key": "date",
      "value": "asc"
    }
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "total_results": 104,
    "orders": [
      {
        "uuid": "9a39a7e0-078b-4321-a6dc-02bb2a505243",
        "is_allocated": false,
        "purchase_order_id": "po-XLisbIUs",
        "created_date": "2018-02-26T17:53:57.326890Z",
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
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
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
            "uuid": "c3fb678f-f881-4894-a7ca-424119289cc4",
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
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
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
: (object) The Sort object contains a Key to sort on and a Direction (dir) to sort in

line_item_statuses
: (array) One or more line item statuses. Will include orders with statuses based upon that `status_conjunction`. Possible Values are: `Unallocated`, `Allocated`, `Rejected`, `HasTracking`, `Backordered`, `Cancelled`. The response will contain orders with statuses that match the provided line_item_status (as combined based on line_item_status_conjunction).

line_item_status_conjunction
: (string) Determines whether search for line_item_statuses returns orders with a union, intersection, or complement of statuses. Possible values: `and`, `or`, `only`. Default: `or`. The conjunction determines whether we return every order that contains all (and), at least one (or), or only (only) the provided line-item-status(es). For conjunction only, line_item_statuses must have exactly one line-item-status.

start_date
: (string) The Start Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

end_date
: (string) The End Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

term
: (string) Term can be Order UUID, PO Number or SKU ID

org_uuids
: (array) An array of Organization Universal Unique Identifiers

##### Sort Object:

key
: (string) The Key is the attribute on which you'd like to sort. Currently this is 'date' only.
dir
: (string) The Direction is ascending or descending.  Use 'asc' for ascending.  Any other value, would return the default direction of descending.

### Response Parameters:

total_results
: (number) The Total Results are the total order count per your oganization

orders
: (list) The list of orders per your organization

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
: (list) The Line Items list contains line items with their uuid, item uuid, item name, sku uuid, sku id, sku name, cost, supplier uuid, supplier name, tracking numbers list, and allocation object.

#### Fees Object:

estimated_shipping_cost
: (number) The Estimated Shipping Cost for the Order

drop_ship_fee
: (number) The Drop Ship Fee for the Order as charged by the Supplier

order_fee
: (number) The Order Fee charged for processing the order through our platform

#### Retailer Object:

name
: (string) The Organization Name within your Retailer account

uuid
: (string) The Universal Unique Identifier for your Organization

user
: (object) The User object contains your name and email address; the name and email address of the user who submitted the Create Order API call.

#### Address Object:

name
: (string) The Name associated with the Address

business_name
: (string) The Business Name associated with the Address

address1
: (string) The First line of the Address

address2
: (string) The Second line of the Address. If an apartment or suite, that information should be entered in this parameter.

city
: (string) The City associated with the Address

state
: (string) The State associated with the Address

postal_code
: (number) The Zip Code / Postal Code associated with the Address

phone_number
: (number) The Phone Number associated with the address

#### Requested Shipping Object:

shipping_carrier
: (string) The Shipping Carrier to deliver the order

shipping_method
: (string) The Shipping Method used by the Shipping Carrier to deliver the order

#### Line Item Object:

uuid
: (string) Universal Unique Identifier for the Line Item

item_uuid
: (string) Universal Unique Identifier for the Item

item_name
: (string) The Item Name

sku_uuid
: (string) The Univeral Unique Identifier for the SKU

sku_id
: (string) The SKU as provided by the Supplier

sku_name
: (string) The SKU Name

status
: (string) The Status for the Line Item. Possible Values are: `Unallocated`, `Allocated`, `Rejected`, `HasTracking`, `Backordered`, `Cancelled`

cost
: (number) The Cost of the SKU

supplier_uuid
: (string) The Universal Unique Identifier for the Supplier

supplier_name
: (string) The Supplier Name

tracking_numbers
: (array) The Tracking Numbers array parameter includes tracking number objects. Each include a tracking number, carrier, method, weight, cost, shipping date, and quantity.

allocation
: (object) The Allocation object contains quantity ordered, quantity allocated, quantity backordered, quantity rejected, and backorder date.

#### Tracking Numbers Object:

tracking_number
: (string) The tracking number for this shipment

shipping_carrier
: (string) The Shipping Carrier for this shipment

shipping_method
: (string) The Shipping Method for this shipment

shipping_weight
: (string) The Shipping Weight for this shipment

shipping_cost
: (number) The Shipping Cost for this shipment

shipping_date
: (string) The date the order was shipped

quantity
: (int) The number of items in the shipment

#### Allocation Object: 

quantity_ordered
: (int) The Quantity Ordered of the SKU

quantity_allocated
: (int) The Quantity Allocated by the Supplier for this Order

quantity_backordered
: (int) The Quantity Backordered is the quantity of the order that cannot be shipped because it is currently in a "backordered" state. If you allow the supplier to fulfill the order, this number is supposed to decrease to 0 as they get the item in-stock in their warehouse(s). When a Supplier gets a Backorder Date, they add it to the field labeled "backorder_date".

quantity_rejected
: (int) The Quantity Rejected by the Supplier is the Quantity that they simply cannot fulfill. Reasons may vary, such as state or federal law, customs, or being out-of-stock on an already discontinued product line.

backorder_date
: (string) The Date that the Backordered SKU will be available for shipment. This date should be used as a tentative schedule which may help determine if waiting for the order is appropriate. Should this date be unacceptable, you may cancel the order with the "Cancel Order" API call.

Expected responses include 200, 400, 401, 403, or 404.


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/orders/" \
     -H 'Authorization: Token dc2ee4bc1b4a87834db8549c0c08fe67e9aabe5d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "line_item_status_conjunction": "or",
  "sort": {
    "key": "date",
    "value": "asc"
  },
  "start": 0,
  "start_date": "2017-07-31T06:00:00.000Z",
  "limit": 2,
  "line_item_statuses": [
    "Unallocated"
  ],
  "end_date": "2018-08-03T06:00:00.000Z",
  "org_uuids": [],
  "term": ""
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/orders/' \
    'Authorization':'Token dc2ee4bc1b4a87834db8549c0c08fe67e9aabe5d' \
    'Content-Type':'application/json; charset=utf-8' \
    line_item_status_conjunction="or" \
    sort:="{
  \"key\": \"date\",
  \"value\": \"asc\"
}" \
    start:=0 \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=2 \
    line_item_statuses:="[
  \"Unallocated\"
]" \
    end_date="2018-08-03T06:00:00.000Z" \
    org_uuids:="[]" \
    term=""

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
                "Authorization": "Token dc2ee4bc1b4a87834db8549c0c08fe67e9aabe5d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    line_item_status_conjunction="or" \
    sort:="{
  \"key\": \"date\",
  \"value\": \"asc\"
}" \
    start:=0 \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=2 \
    line_item_statuses:="[
  \"Unallocated\"
]" \
    end_date="2018-08-03T06:00:00.000Z" \
    org_uuids:="[]" \
    term="")
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
        headers: {"Authorization":"Token dc2ee4bc1b4a87834db8549c0c08fe67e9aabe5d","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"start\":0,\"limit\":2,\"line_item_statuses\":[\"Unallocated\"],\"line_item_status_conjunction\":\"or\",\"start_date\":\"2017-07-31T06:00:00.000Z\",\"end_date\":\"2018-08-03T06:00:00.000Z\",\"term\":\"\",\"org_uuids\":[],\"sort\":{\"key\":\"date\",\"value\":\"asc\"}}")
    request.end();
    

})((error, statusCode, headers, body) => {
    console.log('ERROR:', error); 
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
