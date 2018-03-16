---
title: /products/inventory-lists/&ltinventory_list_uuid&gt/
name: Get Inventory List Detail
position: 2.10
visibility: public
method: get
description: Get the Details of a particular Inventory List you have access to
right_code: |
  ~~~ json
  {
    "uuid": "868ea19d-5081-42ab-a4a5-c2337cd292af",
    "retailer": {
      "uuid": "1d2e146c-a3df-4073-89c6-9ffc3061319c"
    },
    "skus": [
      {
        "uuid": "9060814c-9feb-4a3e-958c-cb26d537cffc"
      },
      {
        "uuid": "12009d4d-6206-4811-9934-10e6016769e8"
      },
      {
        "uuid": "1ba7a1e7-0eb3-46ae-875f-67d65caa94fa"
      }
    ],
    "created": "2017-10-23T18:28:19.509589Z",
    "last_updated": "2017-10-23T18:28:19.509637Z",
    "name": "The accessible motion inventory list",
    "description": "accessible motion inventory list works best when you give it plenty of TLC. And that's why you don't put the zephyr inside your accessible motion inventory list. It doesn't work that way. All your wildest dreams would come true. Oh, no you don't!  Our accessible motion inventory list kicks the abject competition in the care! Be the hero. Be the kind of person your mother wanted you to me. Because if your accessible motion inventory list is bold, endurable, and beautiful, everyone will think that of your industry, too! Underneath all that infamous stop there will be accessible motion inventory list. Watching. Waiting. Wanting. Wishing. Wondering. Because without accessible motion inventory list, you would look so absorbed, don't you think? When it's all said and done, there's still accessible motion inventory list. Still. Because we care about how your accessible motion inventory list looks! You know you want it."
  }
  ~~~
  {: title="Response" }

---
Get the Details of a particular Inventory List you have access to.

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Inventory List

retailer
: (object) The Retailer object contains a single retailer_uuid.

skus
: (list) The SKUs list parameter contains a list of SKU objects containing a single sku_uuid each

created
: (string) The Created parameter is the date the Catalog was Created.

last_updated
: (string) The Last Updated parameter is the date the Catalog was Last Updated.

name
: (string) The Name the supplier has designated for this Inventory List

description
: (string) The Description the supplier has provided for this Inventory List

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
curl "https://api-sandbox.cruxconnect.com/products/inventory-lists/868ea19d-5081-42ab-a4a5-c2337cd292af/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/products/inventory-lists/868ea19d-5081-42ab-a4a5-c2337cd292af/' \
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
    # Get Inventory List Detail
    # GET https://api-sandbox.cruxconnect.com/products/inventory-lists/868ea19d-5081-42ab-a4a5-c2337cd292af/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/products/inventory-lists/868ea19d-5081-42ab-a4a5-c2337cd292af/",
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
// request Get Inventory List Detail
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/inventory-lists/868ea19d-5081-42ab-a4a5-c2337cd292af/',
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
