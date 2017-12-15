---
title: /api/organizations/users/permissions/&ltuser_uuid&gt/
name: Get User Permissions
position: 0.7
type: get
description: Get User Permissions for a particular User
right_code: |
  ~~~ json
  {
    "permissions": [
      {
        "assigned": true,
        "permission": {
          "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
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
          "uuid": "96501d33-b805-418a-b185-267279876ff3",
          "name": "edit_org_users",
          "display_name": "Edit Users",
          "description": "Ability to edit/change/delete users in an organization",
          "visibility": "BOTH",
          "grouping": "ORGUSERS"
        }
      },
      {
        "assigned": true,
        "permission": {
          "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
          "name": "view_org_subscription_plan",
          "display_name": "View Subscription Plan",
          "description": "View the subscription plan info for an organization",
          "visibility": "BOTH",
          "grouping": "ORGSUB"
        }
      }
    }
  }
  ~~~
  {: title="Response" }

---
Get the Permissions on a specified User. This call returns the Permissions in a list which indicates a list of Permissions currently available on the specified User.

### Response Parameters:

#### Permissions List Object:

assigned
: (boolean) Assigned indicates whether the pertinent User has a specific permission

permission
: (object) Permission object contains a uuid, name, display name, description, visibility, and grouping

#### Permission Object:

uuid
: (string) Universal Unique Identifier for a Permission

name
: (string) Name of a Permission; written in shortened snake case

display_name
: (string) Display Name of a Permission; a more user-friendly name of the Permission

description
: (string) Description of a Permission

visibility
: (string) Visibility for writing, reading, or both

grouping
: (string) Grouping where the Permission fits within the aspects of the account type

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl "https://stable.projectthanos.com/api/organizations/users/permissions/3a7acb28-ab13-437e-8c35-46cf4f0bea49/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "notification_via": "email",
  "enabled": "true",
  "notification_frequency": "daily",
  "notification_setting_name": "Foo"
}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://stable.projectthanos.com/api/organizations/users/permissions/3a7acb28-ab13-437e-8c35-46cf4f0bea49/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8' \
    notification_via="email" \
    enabled="true" \
    notification_frequency="daily" \
    notification_setting_name="Foo"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get User Permissions
    # GET https://stable.projectthanos.com/api/organizations/users/permissions/3a7acb28-ab13-437e-8c35-46cf4f0bea49/

    try:
        response = requests.get(
            url="https://stable.projectthanos.com/api/organizations/users/permissions/3a7acb28-ab13-437e-8c35-46cf4f0bea49/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    notification_via="email" \
    enabled="true" \
    notification_frequency="daily" \
    notification_setting_name="Foo")
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
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/organizations/users/permissions/3a7acb28-ab13-437e-8c35-46cf4f0bea49/',
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
    request.write("{\"notification_setting_name\":\"Foo\",\"notification_via\":\"email\",\"enabled\":\"true\",\"notification_frequency\":\"daily\"}")
    request.end();
    

})((error, statusCode, headers, body) => {
    console.log('ERROR:', error); 
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
