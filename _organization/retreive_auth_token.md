---
title: /timp/organizations/user-login/
name: Retrieve Auth Token
position: 2.00
visibility: public
method: post
description: Login to receive an authentication token
right_code: |
  ~~~ json
  {
    "username": "nick@dobaretailer.com",
    "password": "thanos_rocks"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "auth_token": "5d6a1ef8c07df5ccf818aea56a1c23fce89212b0",
    "org_uuid": "f5d2aea7-dcd0-4bb4-bedd-c642ce6fc7a0",
    "user_uuid": "c3fb688d-4aca-42d4-9db1-cc268c465892",
    "retailer_uuid": "cda6b5c7-addf-43d7-bdb3-2fe6a0420c42",
    "supplier_uuid": "",
    "org_type": "RETAILER",
    "permission_assignments": {
      "permissions": [
        {
          "assigned": true,
          "permission": {
            "uuid": "68b1647d-b6a7-48b1-9ec2-bf2f1003b6cc",
            "name": "view_org_users",
            "display_name": "View Users",
            "description": "Ability to see the users in an organization",
            "visibility": "BOTH",
            "grouping": "ORGUSERS"
          }
        },
      ],
      "org_user": {
        "uuid": "c3fb688d-4aca-42d4-9db1-cc268c465892"
      }
    }
  }
  ~~~
  {: title="Response" }

---
Provide a username and password to receive your authentication token and various account-related data. All other calls require an authentication token.

### Request Parameters:

username
: The username you provided for your Retailer or Supplier account

password
: The password you provided for your Retailer or Supplier account

### Response Parameters:

auth_token
: (string) Authentication Token to be used for subsequent API calls (note: authentication tokens expire after two hours of being issued)

org_uuid
: (string) Organization Universal Unique Identifier for the organization

user_uuid
: (string) User Universal Unique Identifier for the particular user making the API call

retailer_uuid
: (string) Universal Unique Identifier for the Retailer - Only provided if logging into a Retailer Account

supplier_uuid
: (string) Universal Unique Identifier for the Supplier - Only provided if logging into a Supplier Account

org_type
: (string) Defines the type of organization based on credentials

permission_assignments
: (object) Permissions assigned status and Organization User ID

#### Permissions Object

permissions
: (object) Contains two parameters assigned -- a boolean value that that shows if the permission is assigned -- and permission object

##### Permission Object

uuid
: (string) Permission UUID

name
: (string) Permission Name.
: {% include links/available_permissions.md %}

display_name
: (string) Permission Display Name

description
: (string) Description of the Permission

visibility
: (string) Visibility based on user type.  This includes 'RETAILER', 'SUPPLIER', or 'BOTH'

grouping
: (string) Permission grouping

#### Organization User Object

uuid
: (string) User's Organization UUID

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/timp/organizations/user-login/" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -u ':' \
     -d $'{
  "username": "nick@dobaretailer.com",
  "password": "thanos_rocks"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/timp/organizations/user-login/' \
    'Authorization':'Basic Og==' \
    'Content-Type':'application/json; charset=utf-8' \
    username="nick@dobaretailer.com" \
    password="thanos_rocks"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Retrieve Auth Token
    # POST https://api-sandbox.cruxconnect.com/timp/organizations/user-login/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/timp/organizations/user-login/",
            headers={
                "Authorization": "Basic Og==",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    username="nick@dobaretailer.com" \
    password="thanos_rocks")
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
// request Retrieve Auth Token
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/organizations/user-login/',
        method: 'POST',
        headers: {"Authorization":"Basic Og==","Content-Type":"application/json; charset=utf-8"}
    };
    httpOptions.headers['User-Agent'] = 'node ' + process.version;

    // Using Basic Auth {"username":"","password":""}

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
    request.write("{\"username\":\"nick@dobaretailer.com\",\"password\":\"thanos_rocks\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
