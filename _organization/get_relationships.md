---
title: /api/organizations/relationships/
name: Get Relationships
position: 0.91
method: get
description: Get all direct Relationships specific to your account
right_code: |
  ~~~ json
  [
    {
      "uuid": "2659c223-8179-4d3f-86aa-340eb35045ad",
      "retailer": {
        "uuid": "1d2e146c-a3df-4073-89c6-9ffc3061319c",
        "organization": {
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "name": "projectthanos",
          "org_type": "RETAILER",
          "status": "ACTIVE",
          "created_date": "2017-10-23T18:20:43.336669Z",
          "active_date": null,
          "account_manager": {
            "uuid": "ad61c73e-790d-4e42-921c-b1d7ccc97217",
            "org_user": {
              "uuid": "817979d4-9d67-4675-a9db-73ac99d9eec7",
              "person": {
                "uuid": "6baf482d-a380-4084-a439-a67b8752f63c",
                "first_name": "Jennifer",
                "last_name": "Garrett",
                "email": "uking@clark-davis.info",
                "phone": "01443719956"
              },
              "status": "ACTIVE"
            }
          }
        }
      },
      "supplier": {
        "uuid": "ce4f9803-7870-4a78-b2cb-8949c8f550d6",
        "organization": {
          "uuid": "1b348539-1f1a-432e-a9c3-63f71e65ad84",
          "name": "Underwood-Chavez",
          "org_type": "SUPPLIER",
          "status": "ACTIVE",
          "created_date": "2017-10-23T18:20:35.835821Z",
          "active_date": null,
          "account_manager": {
            "uuid": "77da8f8f-3c9b-47d0-8043-025372b15015",
            "org_user": {
              "uuid": "5e50b269-1aa8-46c5-9244-a6980b72d0e5",
              "person": {
                "uuid": "82480f25-a531-4e0f-b8eb-caaee42d3e39",
                "first_name": "Kimberly",
                "last_name": "James",
                "email": "hernandezmichael@mann-hunter.biz",
                "phone": "536.461.2834"
              },
              "status": "ACTIVE"
            }
          }
        }
      },
      "status": "ACTIVE",
      "merchandise_manager": null
    },
    {
      "uuid": "2b6df160-9f08-496e-9cc6-f89c17741557",
      "retailer": {
        "uuid": "1d2e146c-a3df-4073-89c6-9ffc3061319c",
        "organization": {
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "name": "projectthanos",
          "org_type": "RETAILER",
          "status": "ACTIVE",
          "created_date": "2017-10-23T18:20:43.336669Z",
          "active_date": null,
          "account_manager": {
            "uuid": "ad61c73e-790d-4e42-921c-b1d7ccc97217",
            "org_user": {
              "uuid": "817979d4-9d67-4675-a9db-73ac99d9eec7",
              "person": {
                "uuid": "6baf482d-a380-4084-a439-a67b8752f63c",
                "first_name": "Jennifer",
                "last_name": "Garrett",
                "email": "uking@clark-davis.info",
                "phone": "01443719956"
              },
              "status": "ACTIVE"
            }
          }
        }
      },
      "status": "ACTIVE",
      "merchandise_manager": null
    },
  ]
  ~~~
  {: title="Response" }

---
Get all of the direct Relationships specific to your account. These Relationships show what suppliers and/or retailers are available to you with related information such as account managers and contact information. Your username and password are optional as you can send your authorization token to receive this information.

### Response Parameters:

#### Relationship Object:

uuid
: (string) Universal Unique Identifier for a Relationship

retailer
: (object) Retailer object containing a uuid, and an organization object

supplier
: (object) Supplier object containing a uuid, and an organization object

status
: (string) Status for the Relationship, which can be "CONFIRMATION WAITING", "ACTIVE", or "DEACTIVATED"

#### Retailer Object:

uuid
: (string) Universal Unique Identifier for a Retailer

organization
: (object) Organization object containing a uuid, name, organization type, status, created date, active date, and an account manager

Supplier:

uuid
: (string) Universal Unique Identifier for the Supplier

organization
: (object) Organization object containing a uuid, name, organization type, status, created date, active date, and an account manager

#### Organization Object:

uuid
: (string) Universal Unique Identifier for an Organization

name
: (string) Name of the Organization

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

#### Account Manager Object:

uuid
: (string) Universal Unique Identifier for an Account Manager

org_user
: (object) Organization User object containing a uuid, person, and status

#### Organization User Object:

uuid
: (string) Universal Unique Identifier for an Organization User

person
: (object) Person object containing a uuid, first name, last name, email address, and phone number

status
: (string) Status for the Organization User, which can be "CONFIRMATION WAITING", "ACTIVE", or "DEACTIVATED"

#### Person Object:

uuid
: (string) Universal Unique Identifier for the Person

first_name
: (string) First Name of the Person

last_name
: (string) Last Name of the Person

email
: (string) Email address of the Person

phone
: (string) Phone number of the Person

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl "https://stable.projectthanos.com/api/organizations/relationships/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://stable.projectthanos.com/api/organizations/relationships/' \
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
    # Get Relationships
    # GET https://stable.projectthanos.com/api/organizations/relationships/

    try:
        response = requests.get(
            url="https://stable.projectthanos.com/api/organizations/relationships/",
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
// request Get Relationships
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/organizations/relationships/',
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
