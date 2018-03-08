---
title: /organizations/connections/
name: Get Connections
position: 1.10
visibility: public
method: get
description: Get all direct Connections specific to your account
right_code: |
  ~~~ json
  [
    {
      "uuid": "4db3ff73-603f-4db6-aaff-ea1acef847a0",
      "retailer": {
        "uuid": "60148a62-008f-4989-9fd2-f79d13cdc6fb",
        "organization": {
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "name": "Crux Retailer",
          "org_type": "RETAILER",
          "status": "ACTIVE",
          "created_date": "2018-02-09T17:02:01Z",
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
          }
        }
      },
      "supplier": {
        "uuid": "b5f05054-dce4-4286-96fc-b9424d6b2137",
        "organization": {
          "uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
          "name": "Crux Supplier A",
          "org_type": "SUPPLIER",
          "status": "ACTIVE",
          "created_date": "2018-02-09T17:02:13Z",
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
          }
        }
      },
      "status": "ACTIVE",
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
      "suppliers_retailer_account_number": null,
      "retailers_supplier_account_number": null
    },
  ]
  ~~~
  {: title="Response" }

---
Get all of the direct Connections specific to your account. These Connections show what suppliers and/or retailers are available to you with related information such as account managers and contact information.

### Response Parameters:

#### Connection Object:

uuid
: (string) Universal Unique Identifier for a Connection

retailer
: (object) Retailer object containing a uuid, and an organization object

supplier
: (object) Supplier object containing a uuid, and an organization object

status
: (string) Status for the Connection, which can be "CONFIRMATION WAITING", "ACTIVE", or "DEACTIVATED"

suppliers_retailer_account_number
: (string) Supplier's retailer account number

retailers_supplier_account_number
: (string) Retailer's supplier account number

{% include objects/retailer.md %}

{% include objects/supplier.md %}

{% include objects/organization.md %}

{% include objects/account_manager.md %}

{% include links/response_codes.md %}

~~~ bash
curl "https://api-sandbox.cruxconnect.com/organizations/connections/" \
     -H 'Authorization: Token d9741c2c241b8f9b9955130ca08dbfbd891d9c84' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/organizations/connections/' \
    'Authorization':'Token d9741c2c241b8f9b9955130ca08dbfbd891d9c84' \
    'Content-Type':'application/json; charset=utf-8'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Connections
    # GET https://api-sandbox.cruxconnect.com/organizations/connections/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/organizations/connections/",
            headers={
                "Authorization": "Token d9741c2c241b8f9b9955130ca08dbfbd891d9c84",
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
// request Get Connections
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/organizations/connections/',
        method: 'GET',
        headers: {"Authorization":"Token d9741c2c241b8f9b9955130ca08dbfbd891d9c84","Content-Type":"application/json; charset=utf-8"}
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
