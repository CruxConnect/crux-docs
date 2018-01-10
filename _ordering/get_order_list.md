---
title: /api/orders/
name: Get Order List
position: 3.00
method: post
description: Get the Order List for your organization
right_code: |
  ~~~ json
  {
    "start": 0,
    "limit": 25,
    "sort": {
      "key": "uuid",
      "dir": "des"
    },
    "line_item_status": [],
    "status_conjuction": "or",
    "start_date": "2017-07-31T06:00:00.000Z",
    "end_date": "2018-08-03T06:00:00.000Z"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "total_results": 3,
    "orders": [
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
            "email": "dchadwick@projectthanos.com"
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
      },
      {
        "uuid": "713ddf6b-1f85-4ce5-86ff-bf6619bf82b4",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "60c34b21-cf25-421d-ab5a-bfe39b0122a6",
        "created_date": "2017-10-23T18:29:24.897608Z",
        "notes": "Sit nihil deleniti quam illum magnam aperiam dolor.",
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
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Emily Greene",
          "business_name": "Wilson Ltd",
          "address1": "Unit 5793 Box 1065\nDPO AP 43179",
          "address2": "606 Stevens Vista Suite 652\nLake Tonyaville, MI 68484-5519",
          "city": "New Jeffreyburgh",
          "state": "Louisiana",
          "postal_code": "50215"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "8e718458-2888-4268-9f40-97cfbc79bd46",
            "item_uuid": "db6537cc-7e4e-4d98-b7e6-7f9044d9de54",
            "item_name": "The enraged destruction item",
            "sku_uuid": "ec26763f-5395-47b7-b7bb-f0ce03058e1d",
            "sku_id": "USaoDXIiLNHOgNy",
            "sku_name": "The enraged destruction item",
            "cost": 12.32,
            "supplier_uuid": "0e9dd1c1-1eb5-45dc-9bb0-fe3d53f9da0d",
            "supplier_name": "Sharp, Green and West",
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
            "uuid": "0b62f1b1-a656-46eb-8d8e-4370174bb1c3",
            "item_uuid": "0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017",
            "item_name": "The capital arch item",
            "sku_uuid": "0cf678be-7dd1-47e3-852c-e80942d5566b",
            "sku_id": "UfvfG2",
            "sku_name": "The capital arch item",
            "cost": 33.16,
            "supplier_uuid": "1b348539-1f1a-432e-a9c3-63f71e65ad84",
            "supplier_name": "Underwood-Chavez",
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
            "uuid": "f44c2907-ade2-4a6e-b235-432036981c5e",
            "item_uuid": "9bd1c686-0ce1-404c-8055-d52e99e2a987",
            "item_name": "The enraged water item",
            "sku_uuid": "31ce0d04-e164-481e-9e41-82c4dff09aac",
            "sku_id": "fic0Sk",
            "sku_name": "The enraged water item",
            "cost": 47.23,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
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
            "uuid": "1e3f529b-7046-457a-9b51-34cee7711b00",
            "item_uuid": "8e1898de-4bee-46ef-b242-16ddfacfd350",
            "item_name": "The innocent competition item",
            "sku_uuid": "260a181a-331e-4e4f-9a57-510048a5d3f2",
            "sku_id": "bpSH45MO",
            "sku_name": "The innocent competition item",
            "cost": 46.53,
            "supplier_uuid": "62bd2059-2f70-4cd5-9944-ba9969fe5f06",
            "supplier_name": "projectzuul",
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
            "uuid": "3a655157-5c23-4742-a0db-0afc9cfa4df6",
            "item_uuid": "8e1898de-4bee-46ef-b242-16ddfacfd350",
            "item_name": "The innocent competition item",
            "sku_uuid": "cffa8102-51d5-4b6a-a847-15ecd542840c",
            "sku_id": "0EdHRMyBgv5sI",
            "sku_name": "The innocent competition item",
            "cost": 18.98,
            "supplier_uuid": "62bd2059-2f70-4cd5-9944-ba9969fe5f06",
            "supplier_name": "projectzuul",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 9,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "de742b48-9a66-49b5-90ca-e7ad5f7c97e4",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "64d42d01-33ef-4ee2-ade1-ce3d581eee6c",
        "created_date": "2017-10-23T18:29:25.120938Z",
        "notes": "Pariatur quidem odio animi deleniti.",
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
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Dylan Simmons",
          "business_name": "Gentry, Thomas and Sloan",
          "address1": "4372 Scott Ranch Suite 626\nTravisborough, CT 32091",
          "address2": "25885 Randy Ways\nMollyfort, OR 78898-2675",
          "city": "Brownview",
          "state": "Washington",
          "postal_code": "27396"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "37d4fd2d-9e92-4198-b24a-5bab45f3f61a",
            "item_uuid": "32ef4bba-1332-4ad2-a599-84fd96be44e5",
            "item_name": "The incomparable arch item",
            "sku_uuid": "94d6d1ed-60d4-4f83-9474-f0fb9c8f6317",
            "sku_id": "LsPsWXJb",
            "sku_name": "The incomparable arch item",
            "cost": 77.1,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
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
            "uuid": "ccd89da0-0258-404b-acb4-e27801f855cd",
            "item_uuid": "89cb0ff0-f524-4bc0-b247-09823cd8c4cc",
            "item_name": "The abnormal cause item",
            "sku_uuid": "9900924d-809e-4430-a863-afd6e7f5e71b",
            "sku_id": "e0l80mJfl47",
            "sku_name": "The abnormal cause item",
            "cost": 57.94,
            "supplier_uuid": "0e9dd1c1-1eb5-45dc-9bb0-fe3d53f9da0d",
            "supplier_name": "Sharp, Green and West",
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
      }
    ]
  }
  ~~~
  {: title="Response" }

---
Get the complete List of Orders for your organization. This list contains all of your orders: completed, incomplete, processing, etc.

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
: (string) Indicates how the line_item_status relates to the order response. Possible values are: `and`, `or`, `all`. Default: `or`. `And` will return all orders that have at least 1 line item matching each supplied status. `or` will return all orders that have at least one line item matching any of the supplied statuses. `only` will return orders that have ALL line items matching the supplied status. Only one line_item_status should be supplied when using `only`.

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
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "limit": 25,
  "status": "New",
  "end_date": "2018-08-03T06:00:00.000Z",
  "sort": {
    "key": "uuid",
    "dir": "des"
  },
  "start_date": "2017-07-31T06:00:00.000Z",
  "start": 0
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://stable.projectthanos.com/api/orders/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8' \
    limit:=25 \
    status="New" \
    end_date="2018-08-03T06:00:00.000Z" \
    sort:="{
  \"key\": \"uuid\",
  \"dir\": \"des\"
}" \
    start_date="2017-07-31T06:00:00.000Z" \
    start:=0

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Order List
    # POST https://stable.projectthanos.com/api/orders/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/orders/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    limit:=25 \
    status="New" \
    end_date="2018-08-03T06:00:00.000Z" \
    sort:="{
  \"key\": \"uuid\",
  \"dir\": \"des\"
}" \
    start_date="2017-07-31T06:00:00.000Z" \
    start:=0)
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
// request Get Order List
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/orders/',
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
    request.write("{\"start\":0,\"limit\":25,\"sort\":{\"key\":\"uuid\",\"dir\":\"des\"},\"status\":\"New\",\"start_date\":\"2017-07-31T06:00:00.000Z\",\"end_date\":\"2018-08-03T06:00:00.000Z\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
