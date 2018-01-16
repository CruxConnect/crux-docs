---
title: /products/catalogs/&ltcatalog_uuid&gt/
name: Get Catalog Detail
position: 2.01
method: get
description: Get the Details of a particular Catalog you have access to
right_code: |
  ~~~ json
  {
    "uuid": "5d704568-d5a6-4751-94ff-cc0d86da99dc",
    "supplier": {
      "uuid": "f2ee86d6-7384-4144-bc35-428cd8e02c16"
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
    "num_skus": 3,
    "default_shipping_cost": null,
    "retailer": {
      "uuid": "1d2e146c-a3df-4073-89c6-9ffc3061319c"
    },
    "created": "2017-10-23T18:25:36.265190Z",
    "last_updated": "2017-10-23T18:25:36.265231Z",
    "name": "The enthusiastic winter catalog",
    "description": "There's just something abounding about cuddling up with your own enthusiastic winter catalog! Even in charming sunlight our enthusiastic winter catalog works like a bed!It will blow your charming mind.Then tacos will start raining right out of the charming sky.Because it's the best enthusiastic winter catalog a person get possibly get.  At least on a charming Tuesday! Our enthusiastic winter catalog comes with built-in stop for that extra emotional flavor.",
    "default_shipping_cost_currency": "USD"
  }
  ~~~
  {: title="Response" }

---
Get the Details of a particular Catalog you have access to.

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Catalog

supplier
: (object) The Supplier object contains a supplier_uuid

skus
: (list) The SKUs list parameter contains a list of SKU objects containing a single sku_uuid each

num_skus
: (number) The total Number of SKUs per the Catalog

default_shipping_cost
: (number) The Default Shipping Cost parameter contains a Shipping Cost the Supplier determined to be the Default. If null or empty, the Supplier has a variable ship cost per the SKUs or a more sophisticated Shipping strategy.

retailer
: (object) The Retailer object contains a single retailer_uuid.

created
: (string) The Created parameter is the date the Catalog was Created.


last_updated
: (string) The Last Updated parameter is the date the Catalog was Last Updated.

name
: (string) The Name the supplier has designated for this Catalog

description
: (string) The Description the supplier has provided for this Catalog

default_shipping_cost_currency
: (string) The Default Shipping Cost Currency parameter indicates what

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
curl "https:/.cruxconnect.com/products/catalogs/5d704568-d5a6-4751-94ff-cc0d86da99dc/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https:/.cruxconnect.com/products/catalogs/5d704568-d5a6-4751-94ff-cc0d86da99dc/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Catalog Detail
    # GET https:/.cruxconnect.com/products/catalogs/5d704568-d5a6-4751-94ff-cc0d86da99dc/

    try:
        response = requests.get(
            url="https:/.cruxconnect.com/products/catalogs/5d704568-d5a6-4751-94ff-cc0d86da99dc/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
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
// request Get Catalog Detail
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api.cruxconnect.com',
        port: '443',
        path: '/products/catalogs/5d704568-d5a6-4751-94ff-cc0d86da99dc/',
        method: 'GET',
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
