---
title: /organizations/reset-password/
name: Reset Password
position: 1.01
visibility: internal
method: post
description: Reset the Password on your account
right_code: |
  ~~~ json
  {
    "email": "user@mycompany.com"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "reset_token": "VBnQ8wmbEuJdoqpAFh01"
  }
  ~~~
  {: title="Response" }

---
Should you need to reset your password, you may initiate the process via this call. This is to be used in conjunction with the ["Validate Password Reset"](#organizationpassword-reset) and ["Create New Password"](#organizationpassword-create) API calls.

### Request Parameters:

email
: (string) The email you provided for your account

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/organizations/reset-password/" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "email": "user@mycompany.com"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/organizations/reset-password/' \
    'Content-Type':'application/json; charset=utf-8' \
    email="user@mycompany.com"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Reset Password
    # POST https://api-sandbox.cruxconnect.com/organizations/reset-password/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/organizations/reset-password/",
            headers={
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    email="user@mycompany.com")
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
// request Reset Password
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/organizations/reset-password/',
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
    request.write("{\"email\":\"user@mycompany.com\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
