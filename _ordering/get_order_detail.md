---
title: /orders/&ltorder_uuid&gt/
name: Get Order Detail
position: 3.02
method: get
description: Get the Details for a specified Order
right_code: |
  ~~~ json
  {
    "uuid": "299fc593-04f0-424d-9847-e359b9dfde56",
    "status": "New",
    "is_allocated": false,
    "purchase_order_id": "bb1e6b18-25fa-4703-8ecb-c4c55da56086",
    "created_date": "2017-10-23T18:29:24.716079Z",
    "notes": "Blanditiis dolores maiores eveniet saepe at.",
    "fees": {
      "estimated_shipping_cost": 0,
      "drop_ship_fee": 0,
      "order_fee": 0
    },
    "retailer": {
      "name": "projectthanos",
      "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
      "user": {
        "name": " ",
        "email": "dchadwick@cruxretailer.com"
      }
    },
    "address": {
      "name": "James Smith",
      "business_name": "Price-Lloyd",
      "address1": "1878 Randy Valleys\nAnthonybury, OH 51137",
      "address2": "127 Cox Spurs\nLake Deborah, PW 48750",
      "city": "Lake Coltonstad",
      "state": "Ohio",
      "postal_code": "90181"
    },
    "requested_shipping": {
      "shipping_carrier": "UPS",
      "shipping_method": "Ground"
    },
    "line_items": [
      {
        "uuid": "abe537ad-d1ee-485e-8f60-920cbd9ba160",
        "item_uuid": "358d6043-220f-4107-93b7-1c22151dd5f0",
        "item_name": "The infamous blood item",
        "sku_uuid": "c3786845-3f06-4a10-a6cd-ff23461ab11f",
        "sku_id": "yl3t2Lij7XJfAnsB",
        "sku_name": "The infamous blood item",
        "status": "unallocated",
        "cost": 58.16,
        "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
        "supplier_name": "Brooks-Jones",
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
        "uuid": "a3efa8a0-c3ef-4dc1-81cc-07a6c5a57e2b",
        "item_uuid": "97fa8fdf-6b94-409e-a684-841d42605881",
        "item_name": "The changeable soap item",
        "sku_uuid": "f0b82bb2-0b12-42bf-b7e4-7195ccfb21ab",
        "sku_id": "utmcbyzttt",
        "sku_name": "The changeable soap item",
        "status": "unallocated",
        "cost": 49.96,
        "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
        "supplier_name": "Flynn Ltd",
        "tracking_numbers": [],
        "allocation": {
          "quantity_ordered": 9,
          "quantity_allocated": 0,
          "quantity_backordered": 0,
          "quantity_rejected": 0,
          "backorder_date": null
        }
      },
      {
        "uuid": "7c997127-19bd-430a-9f61-fdc49fc1527c",
        "item_uuid": "31adb57c-a40a-4a99-b3d0-3c6ccd8e8941",
        "item_name": "The cautious knowledge item",
        "sku_uuid": "9060814c-9feb-4a3e-958c-cb26d537cffc",
        "sku_id": "voGDR4gOyYUOgcT7gw",
        "sku_name": "The cautious knowledge item",
        "status": "unallocated",
        "cost": 2.84,
        "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
        "supplier_name": "Flynn Ltd",
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
        "uuid": "32012bb6-a580-41b7-b1f4-c9f62ced6bc9",
        "item_uuid": "98eb1720-9b1e-49ca-be08-e516e8fb46de",
        "item_name": "The aboard invention item",
        "sku_uuid": "dd9689e9-8241-4a78-afa1-7cbce9b09513",
        "sku_id": "BJA9PlgxiT9kQRaYUMF",
        "sku_name": "The aboard invention item",
        "status": "unallocated",
        "cost": 96.49,
        "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
        "supplier_name": "Brooks-Jones",
        "tracking_numbers": [],
        "allocation": {
          "quantity_ordered": 1,
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

status
: (string) The Status for the Line Item. These can be "unallocated", "allocated", "rejected", "has_tracking", "backordered", and "delivered".

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
curl "https://api-sandbox.cruxconnect.com/orders/299fc593-04f0-424d-9847-e359b9dfde56/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/orders/299fc593-04f0-424d-9847-e359b9dfde56/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Order Detail
    # GET https://api-sandbox.cruxconnect.com/orders/299fc593-04f0-424d-9847-e359b9dfde56/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/orders/299fc593-04f0-424d-9847-e359b9dfde56/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps()
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
        path: '/orders/299fc593-04f0-424d-9847-e359b9dfde56/',
        method: 'GET',
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
    request.write("{}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
