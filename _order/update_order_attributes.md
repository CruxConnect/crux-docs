---
title: /timp/orders/&lt;order_uuid&gt;/attributes/
name: Update Order Attributes
position: 4.07
visibility: public
method: post
description: Update Order Attributes
right_code: |
  ~~~ json
  {
    "retailer_provided_notes": "Jelly donuts for all",
    "supplier_provided_notes": "Jelly donuts for all",
    "retailer_provided_order_attributes": [
      {
        "attribute_name": "dog",
        "attribute_value": "poodle"
      }
    ],
    "supplier_provided_order_attributes": [
      {
        "attribute_name": "cat",
        "attribute_value": "siamese"
      }
    ],
    "line_items": [
      {
        "line_item_uuid": "2c9e67fb-6012-43c4-9bd2-6d6b3129d667",
        "supplier_provided_notes": "Fritters for all",
        "retailer_provided_notes": "Apple Fritters for all",
        "supplier_provided_item_attributes": [
          {
            "attribute_name": "fritter_type",
            "attribute_value": "apple"
          }
        ],
        "retailer_provided_item_attributes": [
          {
            "attribute_name": "fritter_type",
            "attribute_value": "apple raspberry"
          }
        ]
      }
    ]
  }
  ~~~
  {: title="Request" }


---
Update Order Attributes

### URL Parameters:

order_uuid
: (string) The Universal Unique Identifier for the Order

### Request Parameters:

retailer_provided_notes
: (string) Retailer provided notes

supplier_provided_notes
: (string) Supplier provided notes

retailer_provided_order_attributes
: (array) Array of retailer provided Order Attribute objects

supplier_provided_order_attributes
: (array) Array of supplier provided Order Attribute objects

line_items
: (array) Array of line item objects

#### Line Item Objects

line_item_uuid
: (string) Line item Universal Unique Identifier

supplier_provided_notes
: (string) Supplier provided notes

retailer_provided_notes
: (string) Retailer provided notes

supplier_provided_item_attributes
: (array) Array of supplier provided order attribute objects

retailer_provided_item_attributes
: (array) Array of retailer provided order attribute objects

#### Retailer and Supplier Order Attribute Object

{% include timp/orders/attributes.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/timp/orders/3885adeb-3497-4a70-b3fe-4e690aa0a04b/attributes/" \
     -H 'Authorization: Token a9e51a13fc4c02c5dcc02c3f41bf4f5fb9aa36ad' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -H 'Cookie: sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz' \
     -d $'{
  "retailer_provided_order_attributes": [
    {
      "attribute_value": "poodle",
      "attribute_name": "dog"
    }
  ],
  "retailer_provided_notes": "Jelly donuts for all",
  "line_items": [
    {
      "supplier_provided_item_attributes": [
        {
          "attribute_value": "apple",
          "attribute_name": "fritter_type"
        }
      ],
      "line_item_uuid": "2c9e67fb-6012-43c4-9bd2-6d6b3129d667",
      "supplier_provided_notes": "Fritters for all"
    }
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/timp/orders/3885adeb-3497-4a70-b3fe-4e690aa0a04b/attributes/' \
    'Authorization':'Token a9e51a13fc4c02c5dcc02c3f41bf4f5fb9aa36ad' \
    'Content-Type':'application/json; charset=utf-8' \
    'Cookie':'sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz' \
    retailer_provided_order_attributes:="[
  {
    \"attribute_value\": \"poodle\",
    \"attribute_name\": \"dog\"
  }
]" \
    retailer_provided_notes="Jelly donuts for all" \
    line_items:="[
  {
    \"supplier_provided_item_attributes\": [
      {
        \"attribute_value\": \"apple\",
        \"attribute_name\": \"fritter_type\"
      }
    ],
    \"line_item_uuid\": \"2c9e67fb-6012-43c4-9bd2-6d6b3129d667\",
    \"supplier_provided_notes\": \"Fritters for all\"
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
    # Update Order Attributes
    # POST https://api-sandbox.cruxconnect.com/timp/orders/3885adeb-3497-4a70-b3fe-4e690aa0a04b/attributes/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/timp/orders/3885adeb-3497-4a70-b3fe-4e690aa0a04b/attributes/",
            headers={
                "Authorization": "Token a9e51a13fc4c02c5dcc02c3f41bf4f5fb9aa36ad",
                "Content-Type": "application/json; charset=utf-8",
                "Cookie": "sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz",
            },
            data=json.dumps(    retailer_provided_order_attributes:="[
  {
    \"attribute_value\": \"poodle\",
    \"attribute_name\": \"dog\"
  }
]" \
    retailer_provided_notes="Jelly donuts for all" \
    line_items:="[
  {
    \"supplier_provided_item_attributes\": [
      {
        \"attribute_value\": \"apple\",
        \"attribute_name\": \"fritter_type\"
      }
    ],
    \"line_item_uuid\": \"2c9e67fb-6012-43c4-9bd2-6d6b3129d667\",
    \"supplier_provided_notes\": \"Fritters for all\"
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
// request Update Order Attributes
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/orders/3885adeb-3497-4a70-b3fe-4e690aa0a04b/attributes/',
        method: 'POST',
        headers: {"Authorization":"Token a9e51a13fc4c02c5dcc02c3f41bf4f5fb9aa36ad","Content-Type":"application/json; charset=utf-8","Cookie":"sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz"}
    };
    httpOptions.headers['User-Agent'] = 'node ' + process.version;

    // Paw Store Cookies option is not supported

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
    request.write("{\"retailer_provided_notes\":\"Jelly donuts for all\",\"retailer_provided_order_attributes\":[{\"attribute_name\":\"dog\",\"attribute_value\":\"poodle\"}],\"line_items\":[{\"line_item_uuid\":\"2c9e67fb-6012-43c4-9bd2-6d6b3129d667\",\"supplier_provided_notes\":\"Fritters for all\",\"supplier_provided_item_attributes\":[{\"attribute_name\":\"fritter_type\",\"attribute_value\":\"apple\"}]}]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
