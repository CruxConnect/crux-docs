---
title: /organizations/user-login/
name: Retrieve Auth Token
position: 1.00
visibility: public
method: post
description: Login to receive an authentication token
right_code: |
  ~~~ json
  {
    "username": "user@mycompany.com",
    "password": "crux_is_awesome"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "auth_token": "47d4yfbwymedhiudj384702984nakju4hajh395d",
    "org_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
    "user_uuid": "52d13dc7-5463-4f90-9e5b-5b8ec97228ff",
    "retailer_uuid": "",
    "supplier_uuid": "b5f05054-dce4-4286-96fc-b9424d6b2137",
    "org_type": "SUPPLIER",
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
        {
          "assigned": true,
          "permission": {
            "uuid": "293d9373-c318-4724-881c-a4e5b0b3e952",
            "name": "edit_org_users",
            "display_name": "Edit Users",
            "description": "Ability to edit/change/delete users in an organization",
            "visibility": "BOTH",
            "grouping": "ORGUSERS"
          }
        },
      ],
      "org_user": {
        "uuid": "52d13dc7-5463-4f90-9e5b-5b8ec97228ff"
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
: (string) Authentication Token to be used for subsequent API calls

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

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/organizations/user-login/" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -u ':' \
     -d $'{
  "username": "user@mycompany.com",
  "password": "crux_is_awesome"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/organizations/user-login/' \
    'Content-Type':'application/json; charset=utf-8' \
    username="user@mycompany.com" \
    password="crux_is_awesome"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Login
    # POST https://api-sandbox.cruxconnect.com/organizations/user-login/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/organizations/user-login/",
            headers={
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    username="user@mycompany.com" \
    password="crux_is_awesome")
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
// request Login
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/organizations/user-login/',
        method: 'POST',
        headers: {"Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"username\":\"user@mycompany.com\",\"password\":\"crux_is_awesome\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
