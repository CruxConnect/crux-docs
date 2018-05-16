---
title: /orders/create/
name: Create Order - Retailer
position: 5.1.1
visibility: public
method: post
description: Create an Order on your account
right_code: |
  ~~~ json
  {
    "skus": [
      {
        "quantity": "53",
        "sku_id": "bK0bi12ATMo",
        "supplier_uuid": "86ab12cd-fd66-4122-8b81-f837bc72d755",
        "price": "10"
      }
    ],
    "purchase_order_id": "po-tH7poMMX",
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
      "postal_code": "10112",
      "phone_number": "801-555-1212"
    }
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "d87a5566-8a79-44ae-a1f7-938a1ce8babe",
    "is_allocated": false,
    "purchase_order_id": "po-G8pQerR7",
    "created_date": "2018-04-24T01:31:04.750253Z",
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
        "name": "Joe Seller",
        "email": "joe@retailme.com"
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
      "shipping_method": "Ground"
    },
    "line_items": [
      {
        "uuid": "8947c7b8-2308-4e58-8e52-279c1b03a4fc",
        "status": "Unallocated",
        "item_uuid": "5a5fe856-a4bd-4dd2-ac5e-e3c9c29e5ed4",
        "item_name": "The insistent room item",
        "sku_uuid": "43113405-4964-4086-b5cc-9beea7cb127e",
        "sku_id": "bK0bi12ATMo",
        "sku_name": "The insistent room item",
        "sku_title_variants": "The insistent room item {'color': 'azure', 'size': 9}",
        "line_item_special_instructions": null,
        "cost": 18.12,
        "supplier_uuid": "e4ba749a-f899-4a03-a759-4610deb4b5ba",
        "supplier_name": "Morales, Martin and Bautista",
        "tracking_numbers": [],
        "allocation": {
          "quantity_ordered": 71,
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
: (array) The array SKU objects ordered including the supplier_id, sku_id and quantity per SKU

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
<!-- task-github-127 can we starndize SKU objects -->

quantity
: (integer) The Quantity ordered of the SKU ID

sku_id
: (string) The SKU ID is the SKU provided by the supplier which identifies that product you are purchasing

supplier_uuid
: (string) The Supplier Identifier is the ID associated with the Supplier providing the SKU

price
: (decimal) The SKU price (2 decimal places)

expected_sku_cost (optional)
: (decimal) The expected cost of the SKU (2 decimal places)

#### Address Object:

{% include objects/address_business.md %}

### Response Parameters:

uuid
: (string) The Universal Unique Identifier for the Order

status
: (string) The current Status of the Order

is_allocated
: (boolean) Is the order Allocated by the Supplier as of the moment you get the response. Generally, this is false initially as the supplier(s) providing the SKU(s) must allocate for each Order.

purchase_order_id
: (string) The Purchase Order (PO) Identifier for this order. This is the one you provided in the request parameters. It is the Identifer that your organization uses to identify the Order.

created_date
: (string) The Date when the order was created. It will always be the same day as when you send in the request to Create the Order.

notes
: (string) The notes you provided from your request to create the Order. Returns a Max length 250 characters

fees
: (object) The Fees object contains the estimated shipping cost, drop ship fee, and order fee

retailer
: (object) The Retailer object contains an organization name, organization uuid, and a user object

address
: (object) The Address object containing name, business name, address line 1, address line 2, city, state, postal code

requested_shipping
: (object) The Requested Shipping object contains the shipping carrier and shipping method from the request to create the Order.

line_items
: (array) The Line Items contains line items with their uuid, item uuid, item name, sku uuid, sku id, sku name, cost, supplier uuid, supplier name, tracking numbers list, and allocation object.

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

uuid
: (string) Universal Unique Identifier for the Line Item

status
:(string) The Status for the Line Item. Possible Values are: Unallocated, Allocated, Rejected, HasTracking, Backordered, Cancelled

item_uuid
: (string) Universal Unique Identifier for the Item

item_name
: (string) The Item Name

sku_uuid
: (string) The Universal Unique Identifier for the SKU

sku_id
: (string) The SKU as provided by the Supplier

sku_name
: (string) The SKU Name

sku_title_variants
: (string) SKU title variants

line_item_special_instructions
: (string) SKU special instructions

cost
: (decimal) The Cost of the SKU (2 decimal places)

supplier_uuid
: (string) The Universal Unique Identifier for the Supplier

supplier_name
: (string) The Supplier Name

tracking_numbers
: (array) The Tracking Numbers array parameter includes tracking number objects. Each include a tracking number, carrier, method, weight, cost, shipping date, and quantity.

allocation
: (object) The Allocation object contains quantity ordered, quantity allocated, quantity backordered, quantity rejected, and backorder date.

#### Tracking Numbers Object:

{% include objects/tracking_number.md %}

#### Allocation Object:

{% include objects/allocation.md %}

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/orders/create/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "address": {
    "state": "NY",
    "city": "New York",
    "address1": "30 Rockefeller Plaza",
    "business_name": "NBC",
    "postal_code": "10112",
    "phone_number": "801-555-1212",
    "name": "Bob Iger",
    "address2": "STE 123"
  },
  "purchase_order_id": "po-tH7poMMX",
  "notes": "here are some notes",
  "shipping_carrier": "UPS",
  "skus": [
    {
      "quantity": "53",
      "price": "10",
      "sku_id": "bK0bi12ATMo",
      "supplier_uuid": "86ab12cd-fd66-4122-8b81-f837bc72d755"
    }
  ],
  "shipping_method": "Ground"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/orders/create/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    address:="{
  \"state\": \"NY\",
  \"city\": \"New York\",
  \"address1\": \"30 Rockefeller Plaza\",
  \"business_name\": \"NBC\",
  \"postal_code\": \"10112\",
  \"phone_number\": \"801-555-1212\",
  \"name\": \"Bob Iger\",
  \"address2\": \"STE 123\"
}" \
    purchase_order_id="po-tH7poMMX" \
    notes="here are some notes" \
    shipping_carrier="UPS" \
    skus:="[
  {
    \"quantity\": \"53\",
    \"price\": \"10\",
    \"sku_id\": \"bK0bi12ATMo\",
    \"supplier_uuid\": \"86ab12cd-fd66-4122-8b81-f837bc72d755\"
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
    # POST https://api-sandbox.cruxconnect.com/orders/create/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/orders/create/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    address:="{
  \"state\": \"NY\",
  \"city\": \"New York\",
  \"address1\": \"30 Rockefeller Plaza\",
  \"business_name\": \"NBC\",
  \"postal_code\": \"10112\",
  \"phone_number\": \"801-555-1212\",
  \"name\": \"Bob Iger\",
  \"address2\": \"STE 123\"
}" \
    purchase_order_id="po-tH7poMMX" \
    notes="here are some notes" \
    shipping_carrier="UPS" \
    skus:="[
  {
    \"quantity\": \"53\",
    \"price\": \"10\",
    \"sku_id\": \"bK0bi12ATMo\",
    \"supplier_uuid\": \"86ab12cd-fd66-4122-8b81-f837bc72d755\"
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
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/orders/create/',
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
    request.write("{\"skus\":[{\"quantity\":\"53\",\"sku_id\":\"bK0bi12ATMo\",\"supplier_uuid\":\"86ab12cd-fd66-4122-8b81-f837bc72d755\",\"price\":\"10\"}],\"purchase_order_id\":\"po-tH7poMMX\",\"notes\":\"here are some notes\",\"shipping_carrier\":\"UPS\",\"shipping_method\":\"Ground\",\"address\":{\"name\":\"Bob Iger\",\"business_name\":\"NBC\",\"address1\":\"30 Rockefeller Plaza\",\"address2\":\"STE 123\",\"city\":\"New York\",\"state\":\"NY\",\"postal_code\":\"10112\",\"phone_number\":\"801-555-1212\"}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
