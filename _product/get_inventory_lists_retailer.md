---
title: /api/products/inventory-lists/
name: Get Inventory Lists - Retailer
position: 2.09
type: get
description: Get the Inventory Lists for your account
right_code: |
  ~~~ json
  {}
  ~~~
  {: title="Request" }

  ~~~ json
  [
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
    },
    {
      "uuid": "044a84c9-624f-49f1-bb31-29da46dd8aa9",
      "retailer": {
        "uuid": "1d2e146c-a3df-4073-89c6-9ffc3061319c"
      },
      "skus": [
        {
          "uuid": "45d9c4a6-0bf0-4fa6-95df-c421ddba16e5"
        },
        {
          "uuid": "995f5edd-7457-4661-9072-e5e9632d8b21"
        },
        {
          "uuid": "5bd06e80-64ae-4150-bff9-fd3b8896c41c"
        }
      ],
      "created": "2017-10-23T18:28:50.082811Z",
      "last_updated": "2017-10-23T18:28:50.082886Z",
      "name": "The aching hook inventory list",
      "description": "All the other kids with the pumped up kicks will wish they had aching hook inventory list. Be the hero. Because we care about how your aching hook inventory list looks! And then there's our aching hook inventory list, which will blow off your incredible spring!! Even in accessible sunlight our aching hook inventory list works like a water!It will blow your accessible mind.Then tacos will start raining right out of the accessible sky.Because it's the best aching hook inventory list a person get possibly get.  At least on a accessible Tuesday! Because if your aching hook inventory list is bold, chemical, and beautiful, everyone will think that of your thumb, too! When it's all said and done, there's still aching hook inventory list. Still. Because without aching hook inventory list, you would look so elegant, don't you think? It's clear, crisp, and guaranteed! There's just something acidic about cuddling up with your own aching hook inventory list! Be the kind of person your mother wanted you to me. All your wildest dreams would come true. And that's why you don't put the pull inside your aching hook inventory list. It doesn't work that way."
    },
    {
      "uuid": "c9b32603-f6bf-4f49-89fd-8424399974f2",
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
      "created": "2017-10-23T18:27:46.581468Z",
      "last_updated": "2017-10-23T18:27:46.581517Z",
      "name": "The enchanted act inventory list",
      "description": "Because if your enchanted act inventory list is bold, ceaseless, and beautiful, everyone will think that of your spark, too! You know you want it. Oh, no you don't!  Our enchanted act inventory list kicks the impressionable competition in the lake! All the other kids with the pumped up kicks will wish they had enchanted act inventory list. When it's all said and done, there's still enchanted act inventory list. Still. I like, it, I love it, I want some more of it. Because we care about how your enchanted act inventory list looks! Be the kind of person your mother wanted you to me."
    }
  ]
  ~~~
  {: title="Response" }

---
Get the Inventory Lists for your account.

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
curl "https://stable.projectthanos.com/api/products/inventory-lists/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://stable.projectthanos.com/api/products/inventory-lists/' \
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
    # Get List of Inventory Lists - Retailer
    # GET https://stable.projectthanos.com/api/products/inventory-lists/

    try:
        response = requests.get(
            url="https://stable.projectthanos.com/api/products/inventory-lists/",
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
// request Get List of Inventory Lists - Retailer
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/products/inventory-lists/',
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
