---
title: /organizations/all_permissions/
name: Get All Permissions
position: 1.06
visibility: v1
method: get
description: Get all available Permissions
right_code: |
  ~~~ json
  [
    {
      "uuid": "5b7906fd-23dd-4fe1-8e50-778819d145ad",
      "name": "view_org_users",
      "display_name": "View Users",
      "description": "Ability to see the users in an organization",
      "visibility": "BOTH",
      "grouping": "ORGUSERS"
    },
    {
      "uuid": "191b95cc-5555-4947-8085-286d167931ca",
      "name": "edit_org_users",
      "display_name": "Edit Users",
      "description": "Ability to edit/change/delete users in an organization",
      "visibility": "BOTH",
      "grouping": "ORGUSERS"
    },
    {
      "uuid": "64b53e87-01bf-4416-affb-937beea1661e",
      "name": "view_org_subscription_plan",
      "display_name": "View Subscription Plan",
      "description": "View the subscription plan info for an organization",
      "visibility": "BOTH",
      "grouping": "ORGSUB"
    },
  ]
  ~~~
  {: title="Response" }

---
Get all of the available Permissions based on the type of account requested on. These change based on Retailer or Supplier accounts.

To view orgainzation users, you must be assigned the 'view_org_users' permission.
{: .info }

{% include v1/links/available_permissions.md %}

### Response Parameters:

{% include v1/objects/permission.md %}

{% include v1/links/response_codes.md %}

{% include v1/links/response_codes.md %}

~~~ bash
curl "https://api-sandbox.cruxconnect.com/organizations/all_permissions/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/organizations/all_permissions/' \
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
    # Get All Permissions
    # GET https://api-sandbox.cruxconnect.com/organizations/all_permissions/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/organizations/all_permissions/",
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
// request Get All Permissions
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/organizations/all_permissions/',
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
