---
title: /organizations/users/permissions/&ltuser_uuid&gt/
name: Add User Permissions
position: 1.08
visibility: v1
method: patch
description: Add User Permissions for a user of your organization
right_code: |
  ~~~ json
  {
    "permission_uuids": [
      "2a0295b6-dd74-4239-9988-24fcdb1adcea",
      "05a46c58-9d13-4912-9167-7effc2cc7482"
    ]
  }
  ~~~
  {: title="Request" }


---
Add User Permissions allows you to provide a user uuid and Add Permissions if roles change within an organization. Simply provide the user uuid and the permissions list indicating which permissions you wish to add.

To edit organization users, you must be assigned the 'edit_org_users' permission.
{: .info }

### URL Parameters

user_uuid
: (string) User Universal Unique Identifier

### Request Parameters:

permission_uuids
: (string list) The list of permission uuids you wish to remove from a user

{% include v1/links/response_codes.md %}

~~~ bash
curl -X "PATCH" "https://api-sandbox.cruxconnect.com/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "permission_uuids": [
    "2a0295b6-dd74-4239-9988-24fcdb1adcea",
    "05a46c58-9d13-4912-9167-7effc2cc7482"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json PATCH 'https://api-sandbox.cruxconnect.com/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    permission_uuids:="[
  \"2a0295b6-dd74-4239-9988-24fcdb1adcea\",
  \"05a46c58-9d13-4912-9167-7effc2cc7482\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Add User Permissions
    # PATCH https://api-sandbox.cruxconnect.com/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/

    try:
        response = requests.patch(
            url="https://api-sandbox.cruxconnect.com/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    permission_uuids:="[
  \"2a0295b6-dd74-4239-9988-24fcdb1adcea\",
  \"05a46c58-9d13-4912-9167-7effc2cc7482\"
]")
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
// request Add User Permissions
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/',
        method: 'PATCH',
        headers: {"Authorization":"Token 47d4yfbwymedhiudj384702984nakju4hajh395d","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"permission_uuids\":[\"2a0295b6-dd74-4239-9988-24fcdb1adcea\",\"05a46c58-9d13-4912-9167-7effc2cc7482\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
