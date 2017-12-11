---
title: /api/organizations/all_permissions/
name: Get All Permissions
position: 0.6
method: get
description: Get all available Permissions
right_code: |
  ~~~ json
  [
    {
      "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
      "name": "create_org",
      "display_name": "Create Organization",
      "description": "Ability to create an org"
    },
    {
      "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
      "name": "update_org_status",
      "display_name": "Update Org Status",
      "description": "Update the org status pending, active, or deactive"
    },
    {
      "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
      "name": "create_relationships",
      "display_name": "Create Relationship",
      "description": "Add a relationship between organizaitons, such as supplier to retailer"
    }
  ]
  ~~~
  {: title="Response" }

---
Get all of the available Permissions based on the type of account requested on. These change based on Retailer or Supplier accounts. Your username and password are optional as you can send your authorization token to receive this information.

### Response Parameters:

uuid
: (string) Universal Unique Identifier for a Permission

name
: (string) Name of a Permission; written in shortened snake case

display_name
: (string) Display Name of a Permission; a more user-friendly name of the Permission

description
: (string) Description of a Permission

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl "https://stable.projectthanos.com/api/organizations/all_permissions/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://stable.projectthanos.com/api/organizations/all_permissions/' \
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
    # Get All Permissions
    # GET https://stable.projectthanos.com/api/organizations/all_permissions/

    try:
        response = requests.get(
            url="https://stable.projectthanos.com/api/organizations/all_permissions/",
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
// request Get All Permissions
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/organizations/all_permissions/',
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
