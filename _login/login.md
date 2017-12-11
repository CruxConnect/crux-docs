---
title: /api/organizations/user-login/
name: Login
position: 0.0
method: post
description: Login to receive an authentication token
right_code: |
  ~~~ json
  {
    "username": "jweir@projectthanos.com",
    "password": "thanosrocks"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "auth_token": "a0f17278bed479ee719ea890b8caf0329e1f3e5b",
    "org_uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
    "user_uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49",
    "retailer_uuid": "1d2e146c-a3df-4073-89c6-9ffc3061319c",
    "supplier_uuid": "",
    "org_type": "RETAILER"
  }
  ~~~
  {: title="Response" }

---
Provide a username and password to receive your authentication token and various account-related data. The purpose of the authentication token is to allow you to fetch account-related info without using your username and password. Prior to making other account-related calls, login to get your authentication token.

### Request Parameters:

username
: The username you provided for your Retailer or Supplier account

password
: The password you provided for your Retailer or Supplier account

The response will include the following information:

### Response Parameters:

auth_token
: (string) Authentication Token to be used for subsequent API calls

org_uuid
: (string) Organization Universal Unique Identifier for the organization

user_uuid
: (string) User Universal Unique Identifier for the particular user making the API call

retailer_uuid
: (string) Universal Unique Identifier for the Retailer - Only provided if logging into a Retailer Account

supplier_uuid
: (string) Universal Unique Identifier for the Supplier - Only provided if logging into a Supplier Account

org_type
: (string) Defines the type of organization based on credentials

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl -X "POST" "https://stable.projectthanos.com/api/organizations/user-login/" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "username": "jweir@projectthanos.com",
  "password": "thanosrocks"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://stable.projectthanos.com/api/organizations/user-login/' \
    'Content-Type':'application/json; charset=utf-8' \
    username="jweir@projectthanos.com" \
    password="thanosrocks"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Login
    # POST https://stable.projectthanos.com/api/organizations/user-login/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/organizations/user-login/",
            headers={
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    username="jweir@projectthanos.com" \
    password="thanosrocks")
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
// request Login
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/organizations/user-login/',
        method: 'POST',
        headers: {"Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"username\":\"jweir@projectthanos.com\",\"password\":\"thanosrocks\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
