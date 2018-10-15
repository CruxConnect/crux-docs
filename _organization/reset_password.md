---
title: /timp/organizations/reset-password/
name: Reset Password
position: 2.01
visibility: public
method: post
description: Reset the Password on your account
right_code: |
  ~~~ json
  {
    "email": "user@someretailer.com"
  }
  ~~~
  {: title="Request" }


---
Should you need to reset your password, you may initiate the process via this call. This is to be used in conjunction with the ["Validate Password Reset"](#organizationpassword-reset) and ["Create New Password"](#organizationpassword-create) API calls. he reset token expires two hours after issuance.

### Request Parameters:

email
: (string) The email you provided for your account

### Response Parameters:

reset_token
: (string) Reset Token - to be used specifically with "Complete Password Reset" API call

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/timp/organizations/reset-password/" \
     -H 'Authorization: ' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "email": "nick@dobaretailer.com"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/timp/organizations/reset-password/' \
    'Authorization':'' \
    'Content-Type':'application/json; charset=utf-8' \
    email="nick@dobaretailer.com"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Reset Password
    # POST https://api-sandbox.cruxconnect.com/timp/organizations/reset-password/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/timp/organizations/reset-password/",
            headers={
                "Authorization": "",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    email="nick@dobaretailer.com")
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
        path: '/timp/organizations/reset-password/',
        method: 'POST',
        headers: {"Authorization":"","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"email\":\"some@one.com\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
