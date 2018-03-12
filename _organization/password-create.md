---
title: /organizations/complete-password/
name: Create New Password
position: 1.03
visibility: internal
method: post
description: Provide a new password for your account
right_code: |
  ~~~ json
  {
    "password": "crux_is_awesome",
    "token": "VBnQ8wmbEuJdoqpAFh01"
  }
  ~~~
  {: title="Request" }


---
This API call requires that you have first requested to reset your password (["Reset Password" API call](#organizationpassword-reset)) and validated that request (["Validate Password Reset"](#organizationpassword-reset)). To create a new password, you provide the "reset token" that you received in an email sent by the ["Reset Password" API call](#organizationpassword-reset) and provide the password you'd like to use.

### Request Parameters:

password
: (string) The new password you would like to use for your account

token
: (string) This is the "reset_token" you received from your "Reset Password" API call

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/organizations/complete-password/" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "token": "VBnQ8wmbEuJdoqpAFh01",
  "password": "crux_is_awesome"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/organizations/complete-password/' \
    'Content-Type':'application/json; charset=utf-8' \
    token="VBnQ8wmbEuJdoqpAFh01" \
    password="crux_is_awesome"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Create New Password
    # POST https://api-sandbox.cruxconnect.com/organizations/complete-password/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/organizations/complete-password/",
            headers={
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    token="VBnQ8wmbEuJdoqpAFh01" \
    password="crux_is_awesome")
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
// request Create New Password
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/organizations/complete-password/',
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
    request.write("{\"password\":\"crux_is_awesome\",\"token\":\"VBnQ8wmbEuJdoqpAFh01\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
