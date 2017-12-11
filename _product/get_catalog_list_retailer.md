---
title: /api/products/catalogs/
name: Get Catalog List - Retailer
position: 2.00
method: get
description: Get the List of Catalogs you have access to
right_code: |
  ~~~ json
  [
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
    },
    {
      "uuid": "7089b6ff-64f6-4aee-99ea-7d389b301d90",
      "supplier": {
        "uuid": "ce4f9803-7870-4a78-b2cb-8949c8f550d6"
      },
      "skus": [
        {
          "uuid": "a81dc78b-6af2-461c-8a26-6e8d8a3e8b46"
        },
        {
          "uuid": "33d478dc-1a34-472c-84ee-3e7aec7b35f3"
        },
        {
          "uuid": "fef4cf62-fc52-4a22-8485-dbc1dc5d7e88"
        }
      ],
      "num_skus": 3,
      "default_shipping_cost": null,
      "retailer": {
        "uuid": "1d2e146c-a3df-4073-89c6-9ffc3061319c"
      },
      "created": "2017-10-23T18:28:07.027204Z",
      "last_updated": "2017-10-23T18:28:07.027252Z",
      "name": "The enormous pollution catalog",
      "description": "Be the hero. Even in celebrated sunlight our enormous pollution catalog works like a prose!It will blow your celebrated mind.Then tacos will start raining right out of the celebrated sky.Because it's the best enormous pollution catalog a person get possibly get.  At least on a celebrated Tuesday! Be the kind of person your mother wanted you to me. I like, it, I love it, I want some more of it. When it's all said and done, there's still enormous pollution catalog. Still. Because if your enormous pollution catalog is bold, easy-going, and beautiful, everyone will think that of your partner, too! All your wildest dreams would come true. Our enormous pollution catalog comes with built-in room for that extra abject flavor. Because without enormous pollution catalog, you would look so cheerful, don't you think? enormous pollution catalog works best when you give it plenty of TLC. There's just something insignificant about cuddling up with your own enormous pollution catalog! And then there's our enormous pollution catalog, which will blow off your emotional sink!! Oh, no you don't!  Our enormous pollution catalog kicks the aberrant competition in the battle! All the other kids with the pumped up kicks will wish they had enormous pollution catalog.",
      "default_shipping_cost_currency": "USD"
    },
    {
      "uuid": "702c0a58-503e-4bdb-9b9e-e78065c7f120",
      "supplier": {
        "uuid": "9ff4ca63-7a46-4eee-a4fb-859e201460c8"
      },
      "skus": [
        {
          "uuid": "06bcecbc-8e2e-4cae-9b9b-294bcf74836e"
        },
        {
          "uuid": "730c61ee-1f2c-4355-ba72-30e82b14d0b4"
        },
        {
          "uuid": "2925cf50-5382-4c12-b54c-0017411e20df"
        }
      ],
      "num_skus": 3,
      "default_shipping_cost": null,
      "retailer": {
        "uuid": "1d2e146c-a3df-4073-89c6-9ffc3061319c"
      },
      "created": "2017-10-23T18:28:22.720704Z",
      "last_updated": "2017-10-23T18:28:22.720765Z",
      "name": "The capital powder catalog",
      "description": "Oh, no you don't!  Our capital powder catalog kicks the eminent competition in the title! Because without capital powder catalog, you would look so educated, don't you think? Because if your capital powder catalog is bold, elastic, and beautiful, everyone will think that of your pollution, too! Underneath all that insignificant border there will be capital powder catalog. Watching. Waiting. Wanting. Wishing. Wondering. Our capital powder catalog comes with built-in toe for that extra accomplished flavor.",
      "default_shipping_cost_currency": "USD"
    }
  ]
  ~~~
  {: title="Response" }

---
Get the List of Catalogs you have access to. Your username and password are optional as you can send your authorization token to receive this information.

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
curl "https://stable.projectthanos.com/api/products/catalogs/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://stable.projectthanos.com/api/products/catalogs/' \
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
    # Get Catalog List - Retailer
    # GET https://stable.projectthanos.com/api/products/catalogs/

    try:
        response = requests.get(
            url="https://stable.projectthanos.com/api/products/catalogs/",
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
// request Get Catalog List - Retailer
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/products/catalogs/',
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
