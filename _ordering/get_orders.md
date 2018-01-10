---
title: /api/orders/
name: Get Orders
position: 3.00
method: post
description: Get the Orders for your organization
right_code: |
  ~~~ json
  {
    "start": 0,
    "limit": 25,
    "sort": {
      "key": "uuid",
      "dir": "des"
    },
    "line_item_status": [
      "unallocated"
    ],
    "status_conjunction": "or",
    "start_date": "2017-07-31T06:00:00.000Z",
    "end_date": "2018-08-03T06:00:00.000Z"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "total_results": 110,
    "orders": [
      {
        "uuid": "58a5c52c-42c4-4018-bca3-447bb2c146c9",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "86c55b42-fae4-4218-9b8b-40b01c6ec0eb",
        "created_date": "2017-12-05T22:32:32.217413Z",
        "notes": "Ea aperiam ut est iure saepe nemo.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "1bd645dd-f2d8-401b-aa79-cfb990851fe9",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Timothy Gonzalez",
          "business_name": "Hernandez Inc",
          "address1": "225 Le Corners\nAndreaton, ID 14958-4394",
          "address2": "450 Howe Cliff Apt. 557\nThomasfort, ME 36012-3981",
          "city": "Port Ellenfort",
          "state": "Alabama",
          "postal_code": "66445",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "f2cc5d9c-efce-4275-a74a-30fde379e23e",
            "item_uuid": "0c8299b7-a9a4-4399-aef2-dc25702db7a0",
            "item_name": "The eight cobweb item",
            "sku_uuid": "ea6da339-baab-4b90-9f2f-533c58fdc3e3",
            "sku_id": "TESTSKUID",
            "sku_name": "The eight cobweb item",
            "cost": 85.84,
            "supplier_uuid": "b68160e5-61a5-44ce-96d4-40e123cc3450",
            "supplier_name": "Rodriguez-Smith",
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
            "uuid": "37329db8-713e-43b0-8690-c41986e146dd",
            "item_uuid": "a49112fc-5e8b-4d2e-9d63-be9c385714bf",
            "item_name": "The capital river item",
            "sku_uuid": "0ece9413-5a00-4fb5-aaf0-b0ebf5812fd1",
            "sku_id": "ydrMecivyQ5Yleea1R8",
            "sku_name": "The capital river item",
            "cost": 36.27,
            "supplier_uuid": "b68160e5-61a5-44ce-96d4-40e123cc3450",
            "supplier_name": "Rodriguez-Smith",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 2,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "4fc0714f-fc17-492d-8478-665ee1250155",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "05ba256a-efe0-402c-b215-e4bd2e1bd7d9",
        "created_date": "2017-12-05T22:32:32.357963Z",
        "notes": "Itaque iusto suscipit error hic impedit iure odit blanditiis.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "1bd645dd-f2d8-401b-aa79-cfb990851fe9",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Gregory Barnett",
          "business_name": "Hartman Group",
          "address1": "7010 Lynch Forges Suite 356\nWebbland, OH 98141-6408",
          "address2": "36291 Lindsey Extensions\nRoweton, OR 33731-7996",
          "city": "Sabrinastad",
          "state": "Iowa",
          "postal_code": "67896",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "81c4104c-98a1-40d3-8e1d-1b9c45fabab7",
            "item_uuid": "6ae172d7-d201-4893-9562-50069acccfa2",
            "item_name": "The cheeky rule item",
            "sku_uuid": "6c33dd0e-3442-49a3-a247-eb4c8b818173",
            "sku_id": "qNdEi7FHNoSZ8zff6o",
            "sku_name": "The cheeky rule item",
            "cost": 69.8,
            "supplier_uuid": "a3b62a7a-4515-4d26-80d3-9427ce782b37",
            "supplier_name": "Mcknight LLC",
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
            "uuid": "c682fb99-9a3a-4ea3-9dd5-62b5ba448f6a",
            "item_uuid": "f567aa86-4f0e-4997-b485-126fcae5836f",
            "item_name": "The absorbed bite item",
            "sku_uuid": "109f9a9e-b3b0-470f-a9f4-9bdf41d8725a",
            "sku_id": "5HDu63dbVeFOwg",
            "sku_name": "The absorbed bite item",
            "cost": 60.32,
            "supplier_uuid": "0eaac668-e0ae-4b7f-9c71-d240a7f89a4e",
            "supplier_name": "Nelson-Morris",
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
            "uuid": "2ce42622-f879-4055-bafb-8fdd0b0aed93",
            "item_uuid": "2aa4ec0d-e780-467c-b7d5-f1b5322bfa18",
            "item_name": "The impractical knowledge item",
            "sku_uuid": "09800815-8ae9-4a89-b314-a2f13a596fd2",
            "sku_id": "3xHe8rvJPtyyZ0u4WCd",
            "sku_name": "The impractical knowledge item",
            "cost": 1.26,
            "supplier_uuid": "a3b62a7a-4515-4d26-80d3-9427ce782b37",
            "supplier_name": "Mcknight LLC",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 3,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "d84c136d-537e-41f6-83f4-1af4634e02d7",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "b9496bb8-1f6b-4a6d-a613-d4ca8f7ef9b3",
        "created_date": "2017-12-05T22:32:32.529539Z",
        "notes": "Perspiciatis minima impedit dicta perspiciatis quas.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "1bd645dd-f2d8-401b-aa79-cfb990851fe9",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Isaac Carlson",
          "business_name": "Smith-Thornton",
          "address1": "58900 Bentley Drives\nHigginsfort, DE 51542",
          "address2": "85363 Scott Hills Apt. 018\nMayberg, TN 80477",
          "city": "East Christinashire",
          "state": "Massachusetts",
          "postal_code": "85204",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "4801a89f-4943-4f1f-9ff0-20e36853ef4a",
            "item_uuid": "c4bd8f56-9384-440a-978c-4341d1332f2d",
            "item_name": "The cautious pot item",
            "sku_uuid": "7d6e1899-3e23-4818-bed9-1b6dce6fa687",
            "sku_id": "5VsIG6DjjVgZybv",
            "sku_name": "The cautious pot item",
            "cost": 19.2,
            "supplier_uuid": "a3b62a7a-4515-4d26-80d3-9427ce782b37",
            "supplier_name": "Mcknight LLC",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 5,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "fe4ea18a-15cc-4255-a7ed-5354fa1f9a9f",
            "item_uuid": "a49112fc-5e8b-4d2e-9d63-be9c385714bf",
            "item_name": "The capital river item",
            "sku_uuid": "720662af-67da-4eed-8a62-9ab89e581065",
            "sku_id": "4MQPJ7MM6UoEjjI9",
            "sku_name": "The capital river item",
            "cost": 37.82,
            "supplier_uuid": "b68160e5-61a5-44ce-96d4-40e123cc3450",
            "supplier_name": "Rodriguez-Smith",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 10,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "07050fea-f478-4b21-908b-62de98b42261",
            "item_uuid": "f567aa86-4f0e-4997-b485-126fcae5836f",
            "item_name": "The absorbed bite item",
            "sku_uuid": "abf29db5-e627-484b-b328-f67eec5bb048",
            "sku_id": "jiqqvQRjyh4rcOwvAHr",
            "sku_name": "The absorbed bite item",
            "cost": 27.67,
            "supplier_uuid": "0eaac668-e0ae-4b7f-9c71-d240a7f89a4e",
            "supplier_name": "Nelson-Morris",
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
            "uuid": "05156c0c-1801-4fea-9109-2eef5f8acf6b",
            "item_uuid": "5a345ed9-c310-4bc3-b68e-18cedcfe791c",
            "item_name": "The impractical bed item",
            "sku_uuid": "01793e24-4223-47c0-ab77-3523fadafc78",
            "sku_id": "QWXs6zdZ",
            "sku_name": "The impractical bed item",
            "cost": 56.67,
            "supplier_uuid": "a3b62a7a-4515-4d26-80d3-9427ce782b37",
            "supplier_name": "Mcknight LLC",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 7,
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
: (number) The Start is the number of which "Order" you would like to start. If no other filters are used, the default order, which is date created, is used. The default Start value is 0. If this filter is not included in your request, the default value is used.

limit
: (number) The Limit is the element number of "Order" in your Orders List where you would like your results to end. If you have 10 orders and you limit at 8 and start at 4, only orders 4, 5, 6, 7, and 8 are included in the results.

sort
: (object) The Sort object contains a Key to sort on and a Direction (dir) to sort in

line_item_status
: (array) One or more line item statuses: unallocated, allocated, has_tracking, backordered, rejected. The response will contain orders with statuses that match the provided line_item_status (as combined based on status_conjunction)

status_conjunction
: (string) Determines whether search for line_item_status returns orders with a union, intersection, or complement of statuses. Possible values: and, or, only. Default: or. The conjunction determines whether we return every order that contains all (and), at least one (or), or only (only) the provided line-item-status(es). For conjunction only, line_item_status must have exactly one line-item-status.

start_date
: (string) The Start Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

end_date
: (string) The End Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

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

status
: (string) The current Status of the Order (e.g. "New", "Pending", "Complete", "Cancelled")

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
: (string) The Status for the Line Item. Possible Values are: `unallocated`, `allocated`, `rejected`, `has_tracking`, `backordered`

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
: (number) The Quantity Ordered of the SKU

quantity_allocated
: (number) The Quantity Allocated by the Supplier for this Order

quantity_backordered
: (number) The Quantity Backordered is the quantity of the order that cannot be shipped because it is currently in a "backordered" state. If you allow the supplier to fulfill the order, this number is supposed to decrease to 0 as they get the item in-stock in their warehouse(s). When a Supplier gets a Backorder Date, they add it to the field labeled "backorder_date".

quantity_rejected
: (number) The Quantity Rejected by the Supplier is the Quantity that they simply cannot fulfill. Reasons may vary, such as state or federal law, customs, or being out-of-stock on an already discontinued product line.

backorder_date
: (string) The Date that the Backordered SKU will be available for shipment. This date should be used as a tentative schedule which may help determine if waiting for the order is appropriate. Should this date be unacceptable, you may cancel the order with the "Cancel Order" API call.

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl -X "POST" "https://stable.projectthanos.com/api/orders/" \
     -H 'Authorization: Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "sort": {
    "key": "uuid",
    "dir": "des"
  },
  "start": 0,
  "status_conjunction": "or",
  "start_date": "2017-07-31T06:00:00.000Z",
  "limit": 25,
  "line_item_status": [
    "unallocated"
  ],
  "end_date": "2018-08-03T06:00:00.000Z"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://stable.projectthanos.com/api/orders/' \
    'Authorization':'Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c' \
    'Content-Type':'application/json; charset=utf-8' \
    sort:="{
  \"key\": \"uuid\",
  \"dir\": \"des\"
}" \
    start:=0 \
    status_conjunction="or" \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=25 \
    line_item_status:="[
  \"unallocated\"
]" \
    end_date="2018-08-03T06:00:00.000Z"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Orders
    # POST https://stable.projectthanos.com/api/orders/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/orders/",
            headers={
                "Authorization": "Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    sort:="{
  \"key\": \"uuid\",
  \"dir\": \"des\"
}" \
    start:=0 \
    status_conjunction="or" \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=25 \
    line_item_status:="[
  \"unallocated\"
]" \
    end_date="2018-08-03T06:00:00.000Z")
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
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/orders/',
        method: 'POST',
        headers: {"Authorization":"Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"start\":0,\"limit\":25,\"sort\":{\"key\":\"uuid\",\"dir\":\"des\"},\"line_item_status\":[\"unallocated\"],\"status_conjunction\":\"or\",\"start_date\":\"2017-07-31T06:00:00.000Z\",\"end_date\":\"2018-08-03T06:00:00.000Z\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }

