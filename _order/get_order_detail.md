---
title: /timp/orders/&ltuuid&gt/
name: Get Order Detail
position: 4.01
visibility: public
method: get
description: Get the Details for a specified Order
right_code: |
  ~~~ json
  {
    "order_uuid": "f7bc1028-844c-44ca-82df-fe76282d2a8b",
    "po_number": "po-5527771067",
    "created_date": "2018-08-23T16:07:35.864274Z",
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
    "sent_to_supplier": false,
    "retailer": {
      "uuid": "ebf3657c-2abb-4aff-be70-69082acc9302",
      "organization_name": "projectthanos",
      "order_submitted_by": null
    },
    "retailer_provided_order_notes": null,
    "supplier_provided_order_notes": null,
    "retailer_provided_fees": {
      "order_fee": 0.99,
      "order_tax": 2.97,
      "shipping_cost": 7.99,
      "dropship_fee": 0.5
    },
    "retailer_provided_order_attributes": null,
    "supplier_provided_order_attributes": null,
    "invoices": [
    {
      "invoice_items": [
        {
          "sku_id": "56",
          "quantity_ordered": 10,
          "quantity_invoiced": 6,
          "supplier_order_number": "third",
          "invoice_item_attributes": [
            {
              "attribute_name": "invoice item name",
              "attribute_value": "can't believe we need invoice item attribute names and values"
            }
          ]
        }
      ],
      "invoice_number": "abcdef-ghi",
      "invoice_attributes": [
        {
          "attribute_name": "invoice attribute name",
          "attribute_value": "invoice attribute value"
        }
      ]
    }
  ],
    "line_items": [
      {
        "line_item_uuid": "5e91d918-67e8-4957-a69a-df9d2072ad9b",
        "status": "Unallocated",
        "line_item_designation": null,
        "item_uuid": "3bb5ef3b-2f1e-41da-bd85-1d6c746b0fa8",
        "item_name": null,
        "sku_uuid": "841ca56b-26f8-4d45-ac25-5b40d1da7354",
        "sku_id": "7FZvMyg0BjfewNJJ",
        "sku_name": null,
        "sku_title_variants": "None {}",
        "product_codes": {
          "upca": null,
          "ean13": null,
          "isbn": null,
          "gtin14": null,
          "asin": null,
          "mpn": null
        },
        "supplier_item_notes": null,
        "retailer_item_notes": null,
        "retailer_provided_sku_cost": 27.2,
        "supplier": {
          "uuid": "d6ac857d-c844-4312-8485-6d121d065308",
          "organization_name": "Stevens, Smith and Krause",
          "order_submitted_by": null
        },
        "supplier_provided_item_attributes": null,
        "retailer_provided_item_attributes": [
          {
            "attribute_name": "donut",
            "attribute_value": "jelly"
          }
        ],
        "tracking": [
        {
          "tracking_number": "12345",
          "shipping_carrier": "UPS",
          "shipping_method": "Speedy Ground",
          "shipping_weight": null,
          "shipping_cost": 3,
          "shipping_date": "2018-11-12",
          "created_date": "2018-11-10T17:47:07.872391Z",
          "quantity": 10,
          "package_attributes": [
            {
              "attribute_name": "package attribute name",
              "attribute_value": "package attribute value"
            }
          ]
        }
      ],
        "allocation": null
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

retailer_provided_order_notes
: (string) The notes you provided from your request to create the Order.

supplier_provided_order_notes
: (string) The notes provided from the supplier.

fees
: (object) The Fees object contains the estimated shipping cost, drop ship fee, and order fee

retailer
: (object) The Retailer object contains an organization name, organization uuid, and a user object

address
: (object) The Address object containing name, business name, address line 1, address line 2, city, state, postal code

requested_shipping
: (object) The Requested Shipping object contains the shipping carrier and shipping method from the request to create the Order.

retailer_provided_order_attributes
: (array) Retailer provided key/value pair of attributes related to the order

supplier_provided_order_attributes
: (array) Supplier provided key/value pair of attributes related to the order

line_items
: (list) The Line Items list contains line item objects with their uuid, item uuid, item name, sku uuid, sku id, sku name, cost, supplier uuid, supplier name, tracking numbers list, and allocation object.

#### Fees Object:

{% include timp/objects/fees.md %}

#### Retailer Object:

name
: (string) The Organization Name within your Retailer account

uuid
: (string) The Universal Unique Identifier for your Organization

user
: (object) The User object contains your name and email address; the name and email address of the user who submitted the Create Order API call.

#### Address Object:

{% include timp/objects/address_business.md %}

#### Requested Shipping Object:

shipping_carrier
: (string) The Shipping Carrier to deliver the order

shipping_method
: (string) The Shipping Method used by the Shipping Carrier to deliver the order

#### Line Item Object:

{% include timp/objects/line_item.md %}

#### User Object

{% include timp/objects/user_simple.md %}

#### Tracking Number Object:

{% include timp/objects/tracking_number.md %}

#### Allocation Object:

{% include timp/objects/allocation.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/timp/orders/f7bc1028-844c-44ca-82df-fe76282d2a8b/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/timp/orders/f7bc1028-844c-44ca-82df-fe76282d2a8b/' \
    'Authorization':'Token 1234567890' \
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
    # GET https://api-sandbox.cruxconnect.com/timp/orders/f7bc1028-844c-44ca-82df-fe76282d2a8b/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/timp/orders/f7bc1028-844c-44ca-82df-fe76282d2a8b/",
            headers={
                "Authorization": "Token 1234567890",
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
        path: '/timp/orders/f7bc1028-844c-44ca-82df-fe76282d2a8b/',
        method: 'GET',
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
