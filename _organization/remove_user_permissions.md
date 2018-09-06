---
title: /timp/organizations/users/permissions/&lt;user-uuid&gt;/
name: Remove User Permissions
position: 2.09
visibility: public
method: delete
description: Remove User Permissions granted at a prior occasion
right_code: |
  ~~~ json
  {
    "permission_uuids": [
      "5188d840-188d-4066-af79-e073a91eb5a3",
      "e04aec97-79de-450e-b619-8f909e862495"
    ]
  }
  ~~~
  {: title="Request" }


---
Remove User Permissions allows you to provide a user uuid and remove permissions if roles change within an organization. Simply provide the organization uuid, user uuid, and the permissions list indicating which permissions you wish to remove.

To edit organization users, you must be assigned the 'edit_org_users' permission.
{: .info }

### URL Parameters

user_uuid
: (string) User Universal Unique Identifier

### Request Parameters:

permission_uuids
: (string list) The list of permission uuids you wish to remove from a user

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "DELETE" "https://api-sandbox.cruxconnect.com/timp/organizations/users/permissions/c3fb688d-4aca-42d4-9db1-cc268c465892/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "permission_uuids": [
    "5188d840-188d-4066-af79-e073a91eb5a3",
    "e04aec97-79de-450e-b619-8f909e862495"
  ]
}'

~~~
{: title="Curl" }

~~~ bash
http --json DELETE 'https://api-sandbox.cruxconnect.com/timp/organizations/users/permissions/c3fb688d-4aca-42d4-9db1-cc268c465892/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    permission_uuids:="[
  \"5188d840-188d-4066-af79-e073a91eb5a3\",
  \"e04aec97-79de-450e-b619-8f909e862495\"
]"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Remove User Permissions
    # DELETE https://api-sandbox.cruxconnect.com/timp/organizations/users/permissions/c3fb688d-4aca-42d4-9db1-cc268c465892/

    try:
        response = requests.delete(
            url="https://api-sandbox.cruxconnect.com/timp/organizations/users/permissions/c3fb688d-4aca-42d4-9db1-cc268c465892/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    permission_uuids:="[
  \"5188d840-188d-4066-af79-e073a91eb5a3\",
  \"e04aec97-79de-450e-b619-8f909e862495\"
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
// request Remove User Permissions
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/organizations/users/permissions/c3fb688d-4aca-42d4-9db1-cc268c465892/',
        method: 'DELETE',
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
    request.write("{\"permission_uuids\":[\"5188d840-188d-4066-af79-e073a91eb5a3\",\"e04aec97-79de-450e-b619-8f909e862495\"]}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
