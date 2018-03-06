---
title: /organizations/users/permissions/&ltuser_uuid&gt/
name: Remove User Permissions
position: 1.09
visibility: public
method: delete
description: Remove User Permissions granted at a prior occasion
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
Remove User Permissions allows you to provide a user uuid and remove permissions if roles change within an organization. Simply provide the organization uuid, user uuid, and the permissions list indicating which permissions you wish to remove.

To edit organization users, you must be assigned the 'edit_org_users' permission.
{: .info }

### Request Parameters:

permission_uuids
: (string list) The list of permission uuids you wish to remove from a user

{% include links/response_codes.md %}

~~~ bash
curl -X "DELETE" "https://api-sandbox.cruxconnect.com/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/" \
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
http --json DELETE 'https://api-sandbox.cruxconnect.com/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/' \
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
    # Remove User Permissions
    # DELETE https://api-sandbox.cruxconnect.com/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/

    try:
        response = requests.delete(
            url="https://api-sandbox.cruxconnect.com/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/",
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
// request Remove User Permissions
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/organizations/users/permissions/5de38a8e-800e-4cba-84c5-ee6c27f304d8/',
        method: 'DELETE',
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
