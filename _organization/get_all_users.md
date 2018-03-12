---
title: /organizations/users/all/
name: Get All Users
position: 1.04
visibility: public
method: get
description: Get all users, with user details, specific to your account
right_code: |
  ~~~ json
  [
    {
      "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49",
      "person": {
        "uuid": "2e0ecb7e-9426-4e66-a8a9-e69cd8c806c0",
        "first_name": "Crux ",
        "last_name": "User",
        "email": "user@mycompany.com",
        "phone": "1-722-036-2568x9442"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          }
        ],
        "org_user": {
          "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "cefc9200-91eb-40dd-8937-d8edaa8f955f",
      "person": {
        "uuid": "2de10d50-c595-48c3-8cb2-029afd221637",
        "first_name": "Crux",
        "last_name": "User",
        "email": "user@mycompany.com",
        "phone": "(617)395-2696"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          }
        ],
        "org_user": {
          "uuid": "cefc9200-91eb-40dd-8937-d8edaa8f955f"
        }
      },
      "status": "ACTIVE"
    },
  ]
  ~~~
  {: title="Response" }

---
Get all the details about the users on your account. This displays their name, email, phone number, permissions (roles), and more.

To view orgainzation users, you must be assigned the 'view_org_users' permission.
{: .info }

### Response Parameters:

{% include objects/user.md %}

{% include objects/permissions_assignment.md %}

{% include links/response_codes.md %}

~~~ bash
curl "https://api-sandbox.cruxconnect.com/organizations/users/all/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/organizations/users/all/' \
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
    # Get All Users
    # GET https://api-sandbox.cruxconnect.com/organizations/users/all/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/organizations/users/all/",
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
// request Get All Users
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/organizations/users/all/',
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
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
