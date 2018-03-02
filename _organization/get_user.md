---
title: /organizations/users/detail/9c6c7f88-6042-4601-b537-3b141842978d/
name: Get User
position: 0.5
method: get
description: Get all details about a single user on your account
right_code: |
  ~~~ json
  {
    "uuid": "9c6c7f88-6042-4601-b537-3b141842978d",
    "person": {
      "uuid": "fbbf086e-1e57-48b4-9df4-fad9ecda7cde",
      "first_name": "owner",
      "last_name": "user",
      "email": "owneruser8@projectzuul.com",
      "phone": "+54(3)4615639912",
      "job_title": null
    },
    "permission_assignments": {
      "permissions": [
        {
          "assigned": false,
          "permission": {
            "uuid": "5b7906fd-23dd-4fe1-8e50-778819d145ad",
            "name": "view_org_users",
            "display_name": "View Users",
            "description": "Ability to see the users in an organization",
            "visibility": "BOTH",
            "grouping": "ORGUSERS"
          }
        },
      ],
      "org_user": {
        "uuid": "9c6c7f88-6042-4601-b537-3b141842978d"
      }
    },
    "status": "ACTIVE"
  }
  ~~~
  {: title="Response" }

---
Get all the details about a specific user on your Retailer or Supplier account. This displays their name, email, phone number, permissions (roles), and more. For this particular call, the user's uuid must be added to the URL endpoint.

URL Endpoint: /api/organizations/users/detail/<user_uuid>/

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

{% include links/response_codes.md %}


~~~ bash
curl "https://api-dev.cruxconnect.com/organizations/users/detail/9c6c7f88-6042-4601-b537-3b141842978d/" \
     -H 'Authorization: Token f48c0bbe50aedb45dfa70e466cf6e2d328092d5a' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-dev.cruxconnect.com/organizations/users/detail/9c6c7f88-6042-4601-b537-3b141842978d/' \
    'Authorization':'Token f48c0bbe50aedb45dfa70e466cf6e2d328092d5a' \
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
    # GET https://api-dev.cruxconnect.com/organizations/users/detail/9c6c7f88-6042-4601-b537-3b141842978d/

    try:
        response = requests.get(
            url="https://api-dev.cruxconnect.com/organizations/users/detail/9c6c7f88-6042-4601-b537-3b141842978d/",
            headers={
                "Authorization": "Token f48c0bbe50aedb45dfa70e466cf6e2d328092d5a",
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
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/organizations/users/detail/9c6c7f88-6042-4601-b537-3b141842978d/',
        method: 'GET',
        headers: {"Authorization":"Token f48c0bbe50aedb45dfa70e466cf6e2d328092d5a","Content-Type":"application/json; charset=utf-8"}
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
