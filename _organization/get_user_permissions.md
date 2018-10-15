---
title: /timp/organizations/users/permissions/&lt;user-uuid&gt;/
name: Get User Permissions
position: 2.07
visibility: public
method: get
description: Get User Permissions for a particular User
right_code: |
  ~~~ json
  {}
  ~~~
  {: title="Request" }

  ~~~ json
  {
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
  ~~~
  {: title="Response" }

---
Get the Permissions on a specified User. This call returns the Permissions in a list which indicates a list of Permissions currently available on the specified User.

To view orgainzation users, you must be assigned the 'view_org_users' permission.
{: .info }

{% include timp/links/available_permissions.md %}

### URL Parameters

user_uuid
: (string) User Universal Unique Identifier

### Response Parameters:

{% include timp/objects/permissions_list.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/timp/organizations/users/permissions/c3fb688d-4aca-42d4-9db1-cc268c465892/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/timp/organizations/users/permissions/c3fb688d-4aca-42d4-9db1-cc268c465892/' \
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
    # Get User Permissions
    # GET https://api-sandbox.cruxconnect.com/timp/organizations/users/permissions/c3fb688d-4aca-42d4-9db1-cc268c465892/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/timp/organizations/users/permissions/c3fb688d-4aca-42d4-9db1-cc268c465892/",
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
// request Get User Permissions
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/organizations/users/permissions/c3fb688d-4aca-42d4-9db1-cc268c465892/',
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
