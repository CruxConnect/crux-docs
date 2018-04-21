---
title: /orders/&ltorder-uuid&gt/
name: Get Order Detail
position: 6.01
visibility: public
method: get
description: Get the Details for a specified Order
right_code: |

  ~~~ json
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
      "business_name": "Disney",
      "address1": "1955 Mickey Mouse Lane",
      "address2": "STE 123",
      "city": "Anaheim",
      "state": "CA",
      "postal_code": "92802",
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
          "quantity_ordered": 202,
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
Get the Details for a specified Order. This includes the identifiers for the order, universal unique identifier for the order, po number, SKU(s) ordered, and details on the destination, receiver, etc.

### URL Parameters

uuid
: (string) The Universal Unique Identifier for the Order

### Response Parameters:

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
: (list) The Line Items list contains line item objects with their uuid, item uuid, item name, sku uuid, sku id, sku name, cost, supplier uuid, supplier name, tracking numbers list, and allocation object.

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

#### User Object

{% include objects/user_simple.md %}

#### Tracking Number Object:

{% include objects/tracking_number.md %}

#### Allocation Object:

{% include objects/allocation.md %}

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/orders/49bd2a6d-fe6b-4145-a059-9439289801ae/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d'

~~~
{: title="Curl" }

~~~ bash
http GET 'https://api-sandbox.cruxconnect.com/orders/49bd2a6d-fe6b-4145-a059-9439289801ae/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Get Order Detail
    # GET https://api-sandbox.cruxconnect.com/orders/49bd2a6d-fe6b-4145-a059-9439289801ae/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/orders/49bd2a6d-fe6b-4145-a059-9439289801ae/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
            },
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
// request Get Order Detail
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/orders/49bd2a6d-fe6b-4145-a059-9439289801ae/',
        method: 'GET',
        headers: {"Authorization":"Token 47d4yfbwymedhiudj384702984nakju4hajh395d"}
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
    request.write("")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
