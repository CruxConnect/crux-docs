---
title: /api/orders/create/
name: Create Order - Retailer
position: 3.05
method: post
description: Create an Order on your account
right_code: |
  ~~~ json
  {
    "skus": [
      {
        "quantity": "23",
        "sku_id": "HHL59hE",
        "supplier_id": "12347k-lk8s97-asdlfk-098sdf"
      },
      {
        "quantity": "478",
        "sku_id": "wZtMF91H2tIQ8RU",
        "supplier_id": "12347k-lk8s97-asdlfk-098sdf"
      }
    ],
    "purchase_order_id": "po-SHJ7ffBu",
    "notes": "here are some notes",
    "shipping_carrier": "UPS",
    "shipping_method": "Ground",
    "address": {
      "name": "Bob Iger",
      "business_name": "NBC",
      "address1": "30 Rockefeller Plaza",
      "address2": "STE 123",
      "city": "New York",
      "state": "NY",
      "postal_code": "10112"
    }
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "358cd9ec-de30-45c5-b12b-5e4f78037645",
    "status": "New",
    "is_allocated": false,
    "purchase_order_id": "po-SqDgLVTq",
    "created_date": "2017-10-30T22:21:40.156604Z",
    "notes": "here are some notes",
    "fees": {
      "estimated_shipping_cost": 0,
      "drop_ship_fee": 0,
      "order_fee": 0
    },
    "retailer": {
      "name": "projectthanos",
      "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
      "user": {
        "name": "Jason  Weir",
        "email": "jweir@projectthanos.com"
      }
    },
    "address": {
      "name": "Bob Iger",
      "business_name": "NBC",
      "address1": "30 Rockefeller Plaza",
      "address2": "STE 123",
      "city": "New York",
      "state": "NY",
      "postal_code": "10112"
    },
    "requested_shipping": {
      "shipping_carrier": "UPS",
      "shipping_method": "Ground"
    },
    "line_items": [
      {
        "uuid": "57dd034f-5238-4336-94b9-8cb9b9bbd3ee",
        "item_uuid": "97fa8fdf-6b94-409e-a684-841d42605881",
        "item_name": "The changeable soap item",
        "sku_uuid": "45d9c4a6-0bf0-4fa6-95df-c421ddba16e5",
        "sku_id": "HHL59hE",
        "sku_name": "The changeable soap item",
        "cost": 49.99,
        "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
        "supplier_name": "Flynn Ltd",
        "tracking_numbers": [],
        "allocation": {
          "quantity_ordered": 53,
          "quantity_allocated": 0,
          "quantity_backordered": 0,
          "quantity_rejected": 0,
          "backorder_date": null
        }
      },
      {
        "uuid": "161734ec-cd42-4e00-a4d6-171230437ab3",
        "item_uuid": "97fa8fdf-6b94-409e-a684-841d42605881",
        "item_name": "The changeable soap item",
        "sku_uuid": "995f5edd-7457-4661-9072-e5e9632d8b21",
        "sku_id": "wZtMF91H2tIQ8RU",
        "sku_name": "The changeable soap item",
        "cost": 17.76,
        "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
        "supplier_name": "Flynn Ltd",
        "tracking_numbers": [],
        "allocation": {
          "quantity_ordered": 283,
          "quantity_allocated": 0,
          "quantity_backordered": 0,
          "quantity_rejected": 0,
          "backorder_date": null
        }
      }
    ]
  }
  ~~~
  {: title="Response" }

---
Create an Order on your account. By providing the SKU(s), quantity ordered, destination, etc. you may create an order for fulfillment.

### Request Parameters:

skus
: (list) The list of SKUs ordered including the supplier_id, sku_id and quantity per SKU

purchase_order_id
: (string) The Purchase Order ID that you provide to identify your order

notes
: (string) Notes accompanying the order

shipping_carrier
: (string) The Shipping Carrier to deliver the order

shipping_method
: (string) The Shipping Method used by the Shipping Carrier to deliver the order

address
: (object) The Address object containing name, business name, address line 1, address line 2, city, state, postal code

#### SKU Object:

supplier_id
: (string) The Supplier Identifier is the ID associated with the Supplier providing the SKU

sku_id
: (string) The SKU ID is the SKU provided by the supplier which identifies that product you are purchasing

quantity
: (number) The Quantity ordered of the SKU ID

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

### Response Parameters:

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
| 201  | Created                | The API call was received and the order was created                          |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl -X "POST" "https://stable.projectthanos.com/api/orders/create/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "address": {
    "state": "NY",
    "city": "New York",
    "address1": "30 Rockefeller Plaza",
    "business_name": "NBC",
    "postal_code": "10112",
    "name": "Bob Iger",
    "address2": "STE 123"
  },
  "purchase_order_id": "po-SHJ7ffBu",
  "notes": "here are some notes",
  "shipping_carrier": "UPS",
  "skus": [
    {
      "quantity": "23",
      "sku_id": ""
    },
    {
      "quantity": "478",
      "sku_id": ""
    }
  ],
  "shipping_method": "Ground"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://stable.projectthanos.com/api/orders/create/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8' \
    address:="{
  \"state\": \"NY\",
  \"city\": \"New York\",
  \"address1\": \"30 Rockefeller Plaza\",
  \"business_name\": \"NBC\",
  \"postal_code\": \"10112\",
  \"name\": \"Bob Iger\",
  \"address2\": \"STE 123\"
}" \
    purchase_order_id="po-SHJ7ffBu" \
    notes="here are some notes" \
    shipping_carrier="UPS" \
    skus:="[
  {
    \"quantity\": \"23\",
    \"sku_id\": \"\"
  },
  {
    \"quantity\": \"478\",
    \"sku_id\": \"\"
  }
]" \
    shipping_method="Ground"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Create Order - Retailer
    # POST https://stable.projectthanos.com/api/orders/create/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/orders/create/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    address:="{
  \"state\": \"NY\",
  \"city\": \"New York\",
  \"address1\": \"30 Rockefeller Plaza\",
  \"business_name\": \"NBC\",
  \"postal_code\": \"10112\",
  \"name\": \"Bob Iger\",
  \"address2\": \"STE 123\"
}" \
    purchase_order_id="po-SHJ7ffBu" \
    notes="here are some notes" \
    shipping_carrier="UPS" \
    skus:="[
  {
    \"quantity\": \"23\",
    \"sku_id\": \"\"
  },
  {
    \"quantity\": \"478\",
    \"sku_id\": \"\"
  }
]" \
    shipping_method="Ground")
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
// request Create Order - Retailer
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/orders/create/',
        method: 'POST',
        headers: {"Authorization":"Token a0f17278bed479ee719ea890b8caf0329e1f3e5b","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"skus\":[{\"quantity\":\"23\",\"sku_id\":\"\"},{\"quantity\":\"478\",\"sku_id\":\"\"}],\"purchase_order_id\":\"po-SHJ7ffBu\",\"notes\":\"here are some notes\",\"shipping_carrier\":\"UPS\",\"shipping_method\":\"Ground\",\"address\":{\"name\":\"Bob Iger\",\"business_name\":\"NBC\",\"address1\":\"30 Rockefeller Plaza\",\"address2\":\"STE 123\",\"city\":\"New York\",\"state\":\"NY\",\"postal_code\":\"10112\"}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
