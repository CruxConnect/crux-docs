---
title: /organizations/
name: Get Organization Details
position: 0.93
method: get
description: Get Organization Details specific to your organization
right_code: |
  ~~~ json
  {
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
  ~~~
  {: title="Response" }

---
Get the Details about your Organization including the uuid, name, organization type, status, date created, date activated, and account manager.

### Response Parameters:

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

{% include links/response_codes.md %}

~~~ bash
curl "https://api-sandbox.cruxconnect.com/organizations/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b'

~~~
{: title="Curl" }

~~~ bash
http GET 'https://api-sandbox.cruxconnect.com/organizations/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Get Organization Details
    # GET https://api-sandbox.cruxconnect.com/organizations/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/organizations/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
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
        path: '/organizations/',
        method: 'GET',
        headers: {"Authorization":"Token a0f17278bed479ee719ea890b8caf0329e1f3e5b"}
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
