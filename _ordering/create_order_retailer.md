---
title: /orders/create/
name: Create Order - Retailer
position: 4.06
visibility: public
method: post
description: Create an Order on your account
right_code: |
  ~~~ json
  {
    "skus": [
      {
        "quantity": "36",
        "sku_id": "000078",
        "supplier_uuid": "b5f05054-dce4-4286-96fc-b9424d6b2137",
        "price": "27.99"
      }
    ],
    "purchase_order_id": "po-CLOB25tC",
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
    "uuid": "1ab8e55f-ea7e-4a58-b7d3-db723272dbbd",
    "is_allocated": false,
    "purchase_order_id": "po-xErcaA5u",
    "created_date": "2018-03-12T20:27:39.579586Z",
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
      "phone_number": "801-555-1212",
      "country": null
    },
    "requested_shipping": {
      "shipping_carrier": "UPS",
      "shipping_method": "Ground"
    },
    "line_items": [
      {
        "uuid": "d3842ec4-d1f8-4cf1-860b-b9eeb8a35680",
        "status": "Unallocated",
        "item_uuid": "0d0c2332-8cc6-4768-8417-55bd0b298da7",
        "item_name": "Deltran BT Junior 12 Volt",
        "sku_uuid": "17c4d2c8-a5ae-43b9-aecc-c4d688184395",
        "sku_id": "000078",
        "sku_name": "Deltran BT Junior 12 Volt",
        "sku_title_variants": "Deltran BT Junior 12 Volt {}",
        "sku_special_instructions": null,
        "cost": 22,
        "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
        "supplier_name": "Crux Supplier A",
        "tracking_numbers": [],
        "allocation": {
          "quantity_ordered": 22,
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

{% include objects/sku.md %}

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
: (list) The Line Items list contains line items with their uuid, item uuid, item name, sku uuid, sku id, sku name, cost, supplier uuid, supplier name, tracking numbers list, and allocation object.

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

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/orders/create/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
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
  "purchase_order_id": "po-CLOB25tC",
  "notes": "here are some notes",
  "shipping_carrier": "UPS",
  "skus": [
    {
      "quantity": "36",
      "price": "27.99",
      "sku_id": "000078",
      "supplier_uuid": "b5f05054-dce4-4286-96fc-b9424d6b2137"
    }
  ],
  "shipping_method": "Ground"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/orders/create/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
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
    purchase_order_id="po-CLOB25tC" \
    notes="here are some notes" \
    shipping_carrier="UPS" \
    skus:="[
  {
    \"quantity\": \"36\",
    \"price\": \"27.99\",
    \"sku_id\": \"000078\",
    \"supplier_uuid\": \"b5f05054-dce4-4286-96fc-b9424d6b2137\"
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
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
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
    purchase_order_id="po-CLOB25tC" \
    notes="here are some notes" \
    shipping_carrier="UPS" \
    skus:="[
  {
    \"quantity\": \"36\",
    \"price\": \"27.99\",
    \"sku_id\": \"000078\",
    \"supplier_uuid\": \"b5f05054-dce4-4286-96fc-b9424d6b2137\"
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
    request.write("{\"skus\":[{\"quantity\":\"36\",\"sku_id\":\"000078\",\"supplier_uuid\":\"b5f05054-dce4-4286-96fc-b9424d6b2137\",\"price\":\"27.99\"}],\"purchase_order_id\":\"po-CLOB25tC\",\"notes\":\"here are some notes\",\"shipping_carrier\":\"UPS\",\"shipping_method\":\"Ground\",\"address\":{\"name\":\"Bob Iger\",\"business_name\":\"NBC\",\"address1\":\"30 Rockefeller Plaza\",\"address2\":\"STE 123\",\"city\":\"New York\",\"state\":\"NY\",\"postal_code\":\"10112\",\"phone_number\":\"801-555-1212\"}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
