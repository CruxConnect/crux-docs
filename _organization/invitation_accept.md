---
title: /organizations/accept-invite/&lt;invitation-token&gt;/
name: Accept Crux Invite
position: 1.05
visibility: internal
method: post
description: Validate the account invitation token
right_code: |
  ~~~ json
  {
    "password": "crux_is_awesome"
  }
  ~~~
  {: title="Request" }


---
This API call requires that you have first recieved an email containing an invitatation link. That link will contain an invitation token. Alternatively in a development environment, you may use the token included in the response to the (["Reset Password" API call](#organizationpassword-reset)).

This call will set a password for the account tied to the token and mark the account as active. The associated token expires two hours after issuance.

### URL Parameters:

token
: (string) The invitation token

### Request Parameters:

password
: (string) The invitation token

### Expected Response Codes

| Code | Name       | Meaning                                      |
|------|-----------------------------------------------------------|
| 204  | No Content | The invitation was completed                 |
| 404  | Not Found  | The token is invalid                         |

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "http://localhost/organizations/accept-invite/KUMJLpo0tzFVeC5w1uni/" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "password": "crux_is_awesome"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'http://localhost/organizations/accept-invite/KUMJLpo0tzFVeC5w1uni/' \
    'Content-Type':'application/json; charset=utf-8' \
    password="crux_is_awesome"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Accept Invitation
    # POST http://localhost/organizations/accept-invite/KUMJLpo0tzFVeC5w1uni/

    try:
        response = requests.post(
            url="http://localhost/organizations/accept-invite/KUMJLpo0tzFVeC5w1uni/",
            headers={
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    password="crux_is_awesome")
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
// request Accept Invitation
(function(callback) {
    'use strict';

    const httpTransport = require('http');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'localhost',
        port: '80',
        path: '/organizations/accept-invite/KUMJLpo0tzFVeC5w1uni/',
        method: 'POST',
        headers: {"Content-Type":"application/json; charset=utf-8"}
    };
    httpOptions.headers['User-Agent'] = 'node ' + process.version;

    // Paw Store Cookies option is not supported

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
    request.write("{\"password\":\"crux_is_awesome\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
