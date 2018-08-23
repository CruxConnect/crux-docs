---
title: /timp/orders/&lt;order_uuid&gt;/attributes/
name: Get Order attributes
position: 4.06
visibility: public
method: get
description: Get Order attributes
right_code: |
  ~~~ json
  {}
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "retailer_provided_order_attributes": null,
    "retailer_provided_notes": "jelly donuts for everyone",
    "line_items": [
      {
        "line_item_uuid": "0505d71f-4360-4055-b3e8-0caf51c93491",
        "supplier_provided_notes": null,
        "supplier_provided_order_attributes": [
          {
            "attribute_name": "donut",
            "attribute_value": "jelly"
          }
        ]
      }
    ]
  }
  ~~~
  {: title="Response" }

---
Get Order attributes

### URL Parameters:

order_uuid
: (string) The Universal Unique Identifier for the order


### Response Parameters:

retailer_provided_notes
: (string) Retailer provided notes

retailer_provided_order_attributes
: (array) An array of retailer provided order attribute objects

line_items
: (array) An array of line item objects


#### Line Item Object

line_item_uuid
: (string) The Universal Unique Identifier for the line item

supplier_provided_notes
: (string) Supplier provided notes

supplier_provided_order_attributes
: (array) An array of supplier provided order attribute objects


#### Attribute Object

attribute_name
: (string) Attribute name

attribute_value
: (string) Attribute value

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-dev.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/attributes/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -H 'Cookie: sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-dev.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/attributes/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    'Cookie':'sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Order attributes
    # GET https://api-dev.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/attributes/

    try:
        response = requests.get(
            url="https://api-dev.cruxconnect.com/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/attributes/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
                "Cookie": "sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz",
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
// request Get Order attributes
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/timp/orders/7d16d838-b4f2-4c88-a66c-f8eb0bcbbe4d/attributes/',
        method: 'GET',
        headers: {"Authorization":"Token 1234567890","Content-Type":"application/json; charset=utf-8","Cookie":"sessionid=h9qjyhleectu7aef5pkwma0jn2gxgitz"}
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
