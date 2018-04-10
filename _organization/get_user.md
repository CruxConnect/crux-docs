---
title: /organizations/users/detail/&ltuuid&gt/
name: Get User
position: 1.05
visibility: public
method: get
description: Get all details about a single user on your account
right_code: |
  ~~~ json
  {
    "uuid": "52d13dc7-5463-4f90-9e5b-5b8ec97228ff",
    "person": {
      "uuid": "4b4e8ea4-a3cf-4c63-b34e-e1b9047c1340",
      "first_name": "Crux",
      "last_name": "User",
      "email": "user@mycompany.com",
      "phone": null,
      "job_title": null
    },
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
    },
    "status": "ACTIVE"
  }
  ~~~
  {: title="Response" }

---
Get all the details about a specific user on your Retailer or Supplier account. This displays their name, email, phone number, permissions (roles), and more. For this particular call, the user's uuid must be added to the URL endpoint.

To view orgainzation users, you must be assigned the 'view_org_users' permission.
{: .info }

URL Endpoint: `/api/organizations/users/detail/<user_uuid>/`

### Response Parameters:

{% include objects/user.md %}

{% include objects/permissions_assignment.md %}

{% include links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/organizations/users/detail/52d13dc7-5463-4f90-9e5b-5b8ec97228ff/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/organizations/users/detail/52d13dc7-5463-4f90-9e5b-5b8ec97228ff/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get User
    # GET https://api-sandbox.cruxconnect.com/organizations/users/detail/52d13dc7-5463-4f90-9e5b-5b8ec97228ff/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/organizations/users/detail/52d13dc7-5463-4f90-9e5b-5b8ec97228ff/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
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
// request Get User
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/organizations/users/detail/52d13dc7-5463-4f90-9e5b-5b8ec97228ff/',
        method: 'GET',
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
