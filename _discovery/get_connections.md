---
title: /organizations/connections/
name: Get Connections
position: 3.01
visibility: public
method: get
description: Get all direct Connections specific to your account
right_code: |
  ~~~ json
  [
    {
      "uuid": "6c25c0e3-7c6d-4931-bec9-f4da17c0d743",
      "retailer": {
        "uuid": "7c8ceed8-86c3-4c4f-9b45-8bda5aa665b2",
        "organization": {
          "uuid": "359204cc-c2d9-4827-b739-64c335f9fbd1",
          "name": "projectthanos",
          "website": "projectthanos.com",
          "org_type": "RETAILER",
          "status": "ACTIVE",
          "created_date": "2018-04-06T01:11:40.090603Z",
          "active_date": null,
          "account_manager": {
            "uuid": "6cf0bb8b-442e-43c4-8bbe-bc823e17981e",
            "person": {
              "uuid": "cfcc3db3-dbfd-4019-be0a-2858e08a760a",
              "first_name": "Joe",
              "last_name": "Account",
              "email": "joe@cruxaccountmanager.com",
              "phone": "717.334.5425x58894",
              "job_title": "Account Manager"
            }
          }
        },
        "contact": {
          "uuid": "2bccd690-9ba3-4e9e-bed2-96fe02185031",
          "first_name": "owner",
          "last_name": "user",
          "email": "owneruser7@projectthanos.com",
          "phone": "1-042-505-7676x449",
          "job_title": "Account Manager"
        }
      },
      "supplier": {
        "uuid": "88971331-5e51-47be-a762-536499ad0366",
        "organization": {
          "uuid": "963e4549-712b-42d7-8bd9-34eb21d15ea9",
          "name": "projectzuul",
          "website": "projectzuul.com",
          "org_type": "SUPPLIER",
          "status": "ACTIVE",
          "created_date": "2018-04-06T01:11:42.840360Z",
          "active_date": null,
          "account_manager": null
        },
        "contact": {
          "uuid": "c10a3649-2c2c-4e65-b610-870529d79dce",
          "first_name": "owner",
          "last_name": "user",
          "email": "owneruser8@projectzuul.com",
          "phone": "(971)270-6745",
          "job_title": "Account Manager"
        }
      },
      "status": "ACTIVE",
      "account_manager": {
        "uuid": "6cf0bb8b-442e-43c4-8bbe-bc823e17981e",
        "person": {
          "uuid": "cfcc3db3-dbfd-4019-be0a-2858e08a760a",
          "first_name": "Joe",
          "last_name": "Account",
          "email": "joe@cruxaccountmanager.com",
          "phone": "717.334.5425x58894",
          "job_title": "Account Manager"
        }
      },
      "suppliers_retailer_account_number": "38473",
      "retailers_supplier_account_number": "59830"
    }
  ]
  ~~~
  {: title="Response" }

---
Get all of the direct Connections specific to your account. These Connections show what suppliers and/or retailers are available to you with related information such as account managers and contact information.

### Response Parameters:

uuid
: (string) Universal Unique Identifier for a Connection

retailer
: (object) Retailer object containing a uuid, and an organization object

supplier
: (object) Supplier object containing a uuid, and an organization object

status
: (string) Status for the Connection, which can be "CONFIRMATION WAITING", "ACTIVE", or "DEACTIVATED"

account_manager
: (object) Your assigned account manager

suppliers_retailer_account_number
: (string) Supplier's retailer account number

retailers_supplier_account_number
: (string) Retailer's supplier account number


#### Retailer Object:

uuid
: (string) Universal Unique Identifier for a Retailer

organization
: (object) Organization object containing a uuid, name, organization type, status, created date, active date, and an account manager

contact
: (object) Retailer Contact

#### Supplier:

uuid
: (string) Universal Unique Identifier for the Supplier

organization
: (object) Organization object containing a uuid, name, organization type, status, created date, active date, and an account manager

contact
: (object) Supplier Contact

#### Organization Object:

uuid
: (string) Universal Unique Identifier for an Organization

name
: (string) Name of the Organization

website
: (string) Browser-ready URL for supplier's public-facing website. A URL is 'browser-ready' if we can put it in an internet browser and the website loads. (For some websites that means that the protocol needs to be specified, eg, 'https://www.awesome.com'; for others, the protocol is not required, eg, 'www.verycool.com'.)

org_type
: (string) Organization Type defines if the organization is a "RETAILER" or a "SUPPLIER"

status
: (string) Status for the Organization, which can be "PENDING", "ACTIVE", or "DEACTIVATED"

created_date
: (string) Created Date; the Date when the Organization was Created within our system

active_date
: (string) Active Date; the Date when the Organization became Active within our system

account_manager
: (object) Account Manager object containing a uuid and an organization user

#### Contact Object

{% include objects/contact.md %}

#### Account Manager Object:

uuid
: (string) Universal Unique Identifier for an Account Manager

person
: (object) Person is an object containing a uuid, first name, last name, email, and phone number

#### Person Object:

{% include objects/contact.md %}

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl "https://api-dev.cruxconnect.com/organizations/connections/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-dev.cruxconnect.com/organizations/connections/' \
    'Authorization':'Token 1234567890' \
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
    # GET https://api-dev.cruxconnect.com/organizations/connections/

    try:
        response = requests.get(
            url="https://api-dev.cruxconnect.com/organizations/connections/",
            headers={
                "Authorization": "Token 1234567890",
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
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/organizations/connections/',
        method: 'GET',
        headers: {"Authorization":"Token 1234567890","Content-Type":"application/json; charset=utf-8"}
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
