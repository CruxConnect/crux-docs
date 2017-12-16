---
title: /api/organizations/users/permissions/&ltuser_uuid&gt/
name: Add User Permissions
position: 0.8
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

### Request Parameters:

permission_uuids
: (string list) The list of permission uuids you wish to remove from a user

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 204  | No Content             | The API call was received and the permission removal occurred                |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl -X "PATCH" "https://stable.projectthanos.com/api/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
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
http --json PATCH 'https://stable.projectthanos.com/api/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
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
    # PATCH https://stable.projectthanos.com/api/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/

    try:
        response = requests.patch(
            url="https://stable.projectthanos.com/api/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
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
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/',
        method: 'PATCH',
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
