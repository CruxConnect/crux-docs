---
title: /organizations/users/detail/&ltuser_uuid&gt/
name: Get User
position: 0.5
method: get
description: Get all details about a single user on your account
right_code: |
  ~~~ json
  {
    "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49",
    "person": {
      "uuid": "2e0ecb7e-9426-4e66-a8a9-e69cd8c806c0",
      "first_name": "Jason ",
      "last_name": "Weir",
      "email": "jweir@projectthanos.com",
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
  }
  ~~~
  {: title="Response" }

---
Get all the details about a specific user on your Retailer or Supplier account. This displays their name, email, phone number, permissions (roles), and more. For this particular call, the user's uuid must be added to the URL endpoint.

### Response Parameters:

#### User:

uuid
: (string) Universal Unique Identifier for the User

person
: (object) Person is an object containing a uuid, first name, last name, email, and phone number

permission_assignments
: (object) Permission Assignments is an object containing a list of permissions and an organization User

status
: (string) User's account status which can be "CONFIRMATION WAITING", "ACTIVE", or "DEACTIVATED"

#### Person Object:

uuid
: (string) Universal Unique Identifier for the Person

first_name
: (string) First Name of the Person

last_name
: (string) Last Name of the Person

email
: (string) Email address of the Person

phone
: (string) Phone number of the Person

#### Permission Assignments Object:

permissions
: (object list) Permissions are a list of available individual permissions with details as well as if the permission has been assigned to this User

org_user
: (object) Organization User holds the uuid for the User

#### Permissions List Object:

assigned
: (boolean) Assigned indicates whether this particular Permission has been Assigned to this User

permission
: (object) Permission is an object detailing a specific Permission with a uuid, name, display name, and description

#### Permission Object:

uuid
: (string) Universal Unique Identifier for the Permission

name
: (string) Name of the Permission; written in shortened snake case

display_name
: (string) Display Name of the Permission; a more user-friendly name of the Permission

description
: (string) Description of the Permission

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl "https://api-sandbox.cruxconnect.com/organizations/users/detail/3a7acb28-ab13-437e-8c35-46cf4f0bea49/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: text/plain; charset=utf-8' \
     -d $'{
  "username": "jweir@projectthanos.com",
  "password": "thanosrocks"
}'

~~~
{: title="Curl" }

~~~ bash
http --form GET 'https://api-sandbox.cruxconnect.com/organizations/users/detail/3a7acb28-ab13-437e-8c35-46cf4f0bea49/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'text/plain; charset=utf-8' \
    'data'=$'{
  \"username\": \"jweir@projectthanos.com\",
  \"password\": \"thanosrocks\"
}'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Get User
    # GET https://api-sandbox.cruxconnect.com/organizations/users/detail/3a7acb28-ab13-437e-8c35-46cf4f0bea49/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/organizations/users/detail/3a7acb28-ab13-437e-8c35-46cf4f0bea49/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "text/plain; charset=utf-8",
            },
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
        path: '/organizations/users/detail/3a7acb28-ab13-437e-8c35-46cf4f0bea49/',
        method: 'GET',
        headers: {"Authorization":"Token a0f17278bed479ee719ea890b8caf0329e1f3e5b","Content-Type":"text/plain; charset=utf-8"}
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
    request.write("{\n  \"username\": \"jweir@projectthanos.com\",\n  \"password\": \"thanosrocks\"\n}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
