---
title: /api/products/inventory-lists/
name: Create Inventory List - Retailer
position: 2.11
type: post
description: Create an Inventory List for your account
right_code: |
  ~~~ json
  {
    "name": "New Test Inventory List Name op7bNvJAHkdlwcWghAL4G0pTrQAh6gQS",
    "description": "The Description for the New Test Inventory List Name"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "c8ea2ef5-2093-4ea9-ac19-c6ac9d333e18",
    "retailer": {
      "uuid": "1d2e146c-a3df-4073-89c6-9ffc3061319c"
    },
    "skus": [],
    "created": "2017-11-02T17:07:25.823165Z",
    "last_updated": "2017-11-02T17:07:25.823217Z",
    "name": "New Test Inventory List Name",
    "description": "The Description for the New Test Inventory List Name"
  }
  ~~~
  {: title="Response" }

---
Create an Inventory Lists for your account. This Inventory List eventually will hold all of the SKUs you would like grouped together, at your discretion. To add SKUs to an Inventory List see "Add SKUs" and similarly, to add items to an Inventory List see "Add Items". To Create this Inventory list simply provide your authenticiation token you received at login, with the name and description parameters filled out. Your username and password are optional as you can send your authorization token to receive this information.

### Request Parameters:

name
: (string) The Name of the new Inventory List

description
: (string) The Description for the Inventory List

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Inventory List

retailer
: (object) The Retailer object contains a single retailer_uuid.

supplier
: (object) The Supplier object contains a supplier_uuid

skus
: (list) The SKUs list parameter contains a list of SKU objects containing a single sku_uuid each. This is empty when you create the list

num_skus
: (number) The total Number of SKUs per the Catalog

default_shipping_cost
: (number) The Default Shipping Cost parameter contains a Shipping Cost the Supplier determined to be the Default. If null or empty, the Supplier has a variable ship cost per the SKUs or a more sophisticated Shipping strategy.

created
: (string) The Created parameter is the date the Catalog was Created.

last_updated
: (string) The Last Updated parameter is the date the Catalog was Last Updated.

name
: (string) The Name the supplier has designated for this Catalog

description
: (string) The Description the supplier has provided for this Catalog

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 405  | Method Not Allowed     | Generally, the HTTP verb is not correct for the intended call                |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl -X "POST" "https://stable.projectthanos.com/api/products/inventory-lists/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "name": "New Test Inventory List Name op7bNvJAHkdlwcWghAL4G0pTrQAh6gQS",
  "description": "The Description for the New Test Inventory List Name"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://stable.projectthanos.com/api/products/inventory-lists/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8' \
    name="New Test Inventory List Name op7bNvJAHkdlwcWghAL4G0pTrQAh6gQS" \
    description="The Description for the New Test Inventory List Name"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Create Inventory List - Retailer
    # POST https://stable.projectthanos.com/api/products/inventory-lists/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/products/inventory-lists/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    name="New Test Inventory List Name op7bNvJAHkdlwcWghAL4G0pTrQAh6gQS" \
    description="The Description for the New Test Inventory List Name")
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
// request Create Inventory List - Retailer
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/products/inventory-lists/',
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
    request.write("{\"name\":\"New Test Inventory List Name op7bNvJAHkdlwcWghAL4G0pTrQAh6gQS\",\"description\":\"The Description for the New Test Inventory List Name\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
