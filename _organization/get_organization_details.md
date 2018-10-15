---
title: /timp/organizations/
name: Get Organization Details
position: 2.10
visibility: public
method: get
description: Get Organization Details specific to your organization
right_code: |
  ~~~ json
  {
    "uuid": "f5d2aea7-dcd0-4bb4-bedd-c642ce6fc7a0",
    "name": "Doba Retailer",
    "website": "dobaretailer.com",
    "org_type": "RETAILER",
    "status": "ACTIVE",
    "created_date": "2018-04-06T16:04:33Z",
    "active_date": null,
    "account_manager": {
      "uuid": "6c249798-7564-468d-83de-d98ae8b0b7cf",
      "person": {
        "uuid": "f3548ea5-15ab-459e-9f1a-d982b21e916d",
        "first_name": "Joe",
        "last_name": "Account",
        "email": "joe@cruxaccountmanager.com",
        "phone": "(267)977-0572x195",
        "job_title": null
      }
    },
    "retailer_uuid": "cda6b5c7-addf-43d7-bdb3-2fe6a0420c42",
    "supplier_uuid": ""
  }
  ~~~
  {: title="Response" }

---
Get the Details about your Organization including the uuid, name, organization type, status, date created, date activated, and account manager.

### Response Parameters:

{% include timp/objects/organization.md %}

{% include timp/objects/account_manager.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/timp/organizations/" \
     -H 'Authorization: Token 1234567890'

~~~
{: title="Curl" }

~~~ bash
http GET 'https://api-sandbox.cruxconnect.com/timp/organizations/' \
    'Authorization':'Token 1234567890'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Get Organization Details
    # GET https://api-sandbox.cruxconnect.com/timp/organizations/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/timp/organizations/",
            headers={
                "Authorization": "Token 1234567890",
            },
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
// request Get Organization Details
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/organizations/',
        method: 'GET',
        headers: {"Authorization":"Token 1234567890"}
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
    request.write("")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
