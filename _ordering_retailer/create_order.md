
---
title: /timp/orders/create/
name: Create Order
position: 5.00
visibility: public
method: post
description: Create an Order on your account
right_code: |
  ~~~ json
  {
    "skus": [
      {
        "quantity": "2",
        "sku_id": "841ca56b-26f8-4d45-ac25-5b40d1da7354",
        "supplier_org_uuid": "904e880a-0f8b-4e25-86ff-e63588914c95",
        "retailer_provided_shipping_carrier": "UPS",
        "retailer_provided_shipping_method": "Ground",
        "retailer_line_item_instructions": "Ship seperately as available",
        "retailer_provided_sku_cost": 27.2,
        "retailer_provided_line_item_attributes": [
          {
            "name": "donut",
            "value": "jelly"
          }
        ]
      }
    ],
    "address": {
      "name": "Bob Iger",
      "business_name": "NBC",
      "address1": "30 Rockefeller Plaza",
      "address2": "STE 123",
      "city": "New York",
      "state": "NY",
      "postal_code": "10112",
      "phone_number": "801-555-1212"
    },
    "po_number": "po-BKrxV4jG",
    "retailer_provided_order_fee": 0.99,
    "retailer_provided_tax": 2.97,
    "retailer_provided_shipping_cost": 7.99,
    "retailer_provided_dropship_fee": 0.5,
    "retailer_provided_order_attributes": [
      {
        "name": "donut",
        "value": "jelly"
      }
    ],
    "retailer_provided_notes": "jelly donuts for everyone"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "order_uuid": "83c0227e-c19d-4220-a5d8-d78bff44ae87",
    "messages": ""
  }
  ~~~
  {: title="Response" }

---
Create an Order on your account. By providing the SKU(s), quantity ordered, destination, etc. you may create an order for fulfillment.


### Request Parameters:

skus
: (array) ***Required*** The array SKU objects ordered including the supplier_id, sku_id and quantity per SKU

address
: (object) ***Required*** The Address object containing name, business name, address line 1, address line 2, city, state, postal code

po_number
: (string) ***Required*** The Purchase Order ID that you provide to identify your order

retailer_provided_order_fee
: (decimal) Retailer provided order fee (2 decimal places)

retailer_provided_tax
: (decimal) Retailer provided tax (2 decimal places)

retailer_provided_shipping_cost
: (decimal) Retailer provided shipping cost (2 decimal places)

retailer_provided_dropship_fee
: (decimal) Retailer provided dropship fee (2 decimal places)

retailer_provided_order_attributes
: (array) An array of Retailer provided order attribute objects

retailer_provided_notes
: (string) Retailer provided notes

#### SKU Object:

sku_id
: (string) The SKU ID is the SKU provided by the supplier which identifies that product you are purchasing

quantity
: (integer) ***Required*** The Quantity ordered of the SKU ID

supplier_org_uuid
: (string) ***Required*** The Supplier Identifier is the ID associated with the Supplier providing the SKU

retailer_provided_shipping_carrier
: (string) The Retailer provided shipping carrier

retailer_provided_shipping_method
: (string) The Retailer provided shipping method

retailer_line_item_instructions
: (string) The Retailer provided line item instructions

retailer_provided_sku_cost
: (decimal) The Retailer provided SKU cost (2 decimal places)

retailer_provided_line_item_attributes
: (array) An array of Retailer provided line item attribute objects

#### Address Object:

{% include timp/objects/address_business.md %}

#### Line Item Attribute Object

attribute_name
: (string) Attribute name

attribute_value
: (string) Attribute Value

#### Retailer Provided Order Attribute Object

attribute_name
: (string) Attribute name

attribute_value
: (string) Attribute Value

### Response Parameters:

order_uuid
: (string) The Universal Unique Identifier for the Order

messages
: (array) An array of string messages

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-dev.cruxconnect.com/timp/orders/create/" \
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
  "po_number": "po-BKrxV4jG",
  "retailer_provided_order_fee": 0.99,
  "retailer_provided_tax": 2.97,
  "retailer_provided_dropship_fee": 0.5,
  "retailer_provided_notes": "jelly donuts for everyone",
  "retailer_provided_shipping_cost": 7.99,
  "retailer_provided_order_attributes": [
    {
      "name": "donut",
      "value": "jelly"
    }
  ],
  "skus": [
    {
      "sku_id": "841ca56b-26f8-4d45-ac25-5b40d1da7354",
      "quantity": "2",
      "retailer_provided_shipping_carrier": "UPS",
      "retailer_line_item_instructions": "Ship seperately as available",
      "retailer_provided_sku_cost": 27.2,
      "retailer_provided_line_item_attributes": [
        {
          "name": "donut",
          "value": "jelly"
        }
      ],
      "supplier_org_uuid": "904e880a-0f8b-4e25-86ff-e63588914c95",
      "retailer_provided_shipping_method": "Ground"
    }
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-dev.cruxconnect.com/timp/orders/create/' \
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
    po_number="po-BKrxV4jG" \
    retailer_provided_order_fee:=0.99 \
    retailer_provided_tax:=2.97 \
    retailer_provided_dropship_fee:=0.5 \
    retailer_provided_notes="jelly donuts for everyone" \
    retailer_provided_shipping_cost:=7.99 \
    retailer_provided_order_attributes:="[
  {
    \"name\": \"donut\",
    \"value\": \"jelly\"
  }
]" \
    skus:="[
  {
    \"sku_id\": \"841ca56b-26f8-4d45-ac25-5b40d1da7354\",
    \"quantity\": \"2\",
    \"retailer_provided_shipping_carrier\": \"UPS\",
    \"retailer_line_item_instructions\": \"Ship seperately as available\",
    \"retailer_provided_sku_cost\": 27.2,
    \"retailer_provided_line_item_attributes\": [
      {
        \"name\": \"donut\",
        \"value\": \"jelly\"
      }
    ],
    \"supplier_org_uuid\": \"904e880a-0f8b-4e25-86ff-e63588914c95\",
    \"retailer_provided_shipping_method\": \"Ground\"
  }
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Create Order
    # POST https://api-dev.cruxconnect.com/timp/orders/create/

    try:
        response = requests.post(
            url="https://api-dev.cruxconnect.com/timp/orders/create/",
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
    po_number="po-BKrxV4jG" \
    retailer_provided_order_fee:=0.99 \
    retailer_provided_tax:=2.97 \
    retailer_provided_dropship_fee:=0.5 \
    retailer_provided_notes="jelly donuts for everyone" \
    retailer_provided_shipping_cost:=7.99 \
    retailer_provided_order_attributes:="[
  {
    \"name\": \"donut\",
    \"value\": \"jelly\"
  }
]" \
    skus:="[
  {
    \"sku_id\": \"841ca56b-26f8-4d45-ac25-5b40d1da7354\",
    \"quantity\": \"2\",
    \"retailer_provided_shipping_carrier\": \"UPS\",
    \"retailer_line_item_instructions\": \"Ship seperately as available\",
    \"retailer_provided_sku_cost\": 27.2,
    \"retailer_provided_line_item_attributes\": [
      {
        \"name\": \"donut\",
        \"value\": \"jelly\"
      }
    ],
    \"supplier_org_uuid\": \"904e880a-0f8b-4e25-86ff-e63588914c95\",
    \"retailer_provided_shipping_method\": \"Ground\"
  }
]")
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
// request Create Order
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/timp/orders/create/',
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
    request.write("{\"skus\":[{\"quantity\":\"2\",\"sku_id\":\"841ca56b-26f8-4d45-ac25-5b40d1da7354\",\"supplier_org_uuid\":\"904e880a-0f8b-4e25-86ff-e63588914c95\",\"retailer_provided_shipping_carrier\":\"UPS\",\"retailer_provided_shipping_method\":\"Ground\",\"retailer_line_item_instructions\":\"Ship seperately as available\",\"retailer_provided_sku_cost\":27.2,\"retailer_provided_line_item_attributes\":[{\"name\":\"donut\",\"value\":\"jelly\"}]}],\"address\":{\"name\":\"Bob Iger\",\"business_name\":\"NBC\",\"address1\":\"30 Rockefeller Plaza\",\"address2\":\"STE 123\",\"city\":\"New York\",\"state\":\"NY\",\"postal_code\":\"10112\",\"phone_number\":\"801-555-1212\"},\"po_number\":\"po-BKrxV4jG\",\"retailer_provided_order_fee\":0.99,\"retailer_provided_tax\":2.97,\"retailer_provided_shipping_cost\":7.99,\"retailer_provided_dropship_fee\":0.5,\"retailer_provided_order_attributes\":[{\"name\":\"donut\",\"value\":\"jelly\"}],\"retailer_provided_notes\":\"jelly donuts for everyone\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
