---
title: /orders/
name: Get Orders
position: 0
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
    "line_item_status_conjunction": "or",
    "start_date": "2017-07-31T06:00:00.000Z",
    "end_date": "2018-08-03T06:00:00.000Z",
    "term": "",
    "org_uuids": []
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "total_results": 101,
    "orders": [
      {
        "uuid": "10307ca4-c702-4a44-abb3-3828e67bdbb9",
        "is_allocated": false,
        "purchase_order_id": "4225a169-c912-438c-be13-fcfbf9c6ba5e",
        "created_date": "2018-02-13T23:50:45.118818Z",
        "notes": "Accusamus voluptatem beatae quibusdam quia ex consequatur.",
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
          "name": "Mr. Daniel Morales",
          "business_name": "Gonzalez, Fisher and Richmond",
          "address1": "234 Sandra Cove Suite 835\nJosephfort, ID 04759",
          "address2": "851 Gutierrez Fork\nNorth Marystad, MI 54955",
          "city": "Port Ryanstad",
          "state": "Missouri",
          "postal_code": "28806",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "0f022062-6ec8-4beb-97cf-02fe3d2c5820",
            "status": "Unallocated",
            "item_uuid": "041a4cf0-a4a6-46eb-a61c-a87b28995557",
            "item_name": "Frogg Toggs Pro Lite Rain Suit Royal Blue - X/XXL",
            "sku_uuid": "adc3c7f0-8811-4c56-a968-2d88c9dcfd92",
            "sku_id": "1002664",
            "sku_name": "Frogg Toggs Pro Lite Rain Suit Royal Blue - X/XXL",
            "cost": 39.6,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 8,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "7b90f9d5-6497-48e6-8b70-61f669f8e8d4",
            "status": "Unallocated",
            "item_uuid": "f45deb3e-2f98-41b9-85d6-d50b8f9557f2",
            "item_name": "Spyderco Endura4 Lightweight Black FRN Comboedge",
            "sku_uuid": "4b89350e-27f7-4d55-b643-b8f1d3b64f18",
            "sku_id": "000951",
            "sku_name": "Spyderco Endura4 Lightweight Black FRN Comboedge",
            "cost": 51.38,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 6,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "980b9534-42b1-4c05-8bf1-ff8b5c966d63",
            "status": "Unallocated",
            "item_uuid": "51041ea6-8946-42f7-96a8-ac9ed9a17119",
            "item_name": "Genesis Original Righthand Bow Green",
            "sku_uuid": "e5cc3d99-19ed-4d6e-bef9-1aef50f33c4a",
            "sku_id": "000192",
            "sku_name": "Genesis Original Righthand Bow Green",
            "cost": 68.46,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 3,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "0e29ee59-cc01-4698-b462-84f3b7f43f34",
            "status": "Unallocated",
            "item_uuid": "88d1cee7-9ee3-447e-82cf-0a9591bd1c86",
            "item_name": "Women’s Motivation Tech Bra",
            "sku_uuid": "4e85d942-b411-495a-ad09-3cac30f86244",
            "sku_id": "NF0A2VARFTH-S",
            "sku_name": "Women’s Motivation Tech Bra",
            "cost": 37.21,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 7,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "7c37c3d3-d90c-4f86-8d7c-2ba43ce882dd",
            "status": "Unallocated",
            "item_uuid": "2ba73e2a-bd96-47c9-9317-045101e35674",
            "item_name": "Women’s Freedom Insulated Pant",
            "sku_uuid": "6effebfa-ee19-47f3-8634-f3a3b40967a6",
            "sku_id": "NF0A3337FN4-XL-SHT",
            "sku_name": "Women’s Freedom Insulated Pant",
            "cost": 54.38,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 8,
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
: (string) The Key is the attribute on which you'd like to sort. Possible values include date, status, and sku_id.

dir
: (string) The Direction is ascending or descending entered as "asc" or "des"

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
: (list) The Tracking Numbers list provides a Tracking Number or list of multiple Tracking Numbers for this particular SKU.

allocation
: (object) The Allocation object contains quantity ordered, quantity allocated, quantity backordered, quantity rejected, and backorder date.

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
  "start": 0,
  "start_date": "2017-07-31T06:00:00.000Z",
  "limit": 1,
  "line_item_statuses": [
    "unallocated"
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
    start:=0 \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=1 \
    line_item_statuses:="[
  \"unallocated\"
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
    start:=0 \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=1 \
    line_item_statuses:="[
  \"unallocated\"
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
    request.write("{\"start\":0,\"limit\":1,\"line_item_statuses\":[\"unallocated\"],\"line_item_status_conjunction\":\"or\",\"start_date\":\"2017-07-31T06:00:00.000Z\",\"end_date\":\"2018-08-03T06:00:00.000Z\",\"term\":\"\",\"org_uuids\":[]}")
    request.end();
    

})((error, statusCode, headers, body) => {
    console.log('ERROR:', error); 
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
