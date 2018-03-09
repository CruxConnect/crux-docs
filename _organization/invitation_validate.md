---
title: /organizations/accept-invite/&lt;invitation-token&gt;/
name: Validate Crux Invite
position: 1.04
visibility: internal
method: get
description: Validate the account invitation token
right_code: |
  ~~~ json

  ~~~
  {: title="Request" }

  ~~~ json
  {
    "email": "mrbailey@projectzuul.com",
    "token": "gAhdVJa6r7YzoP54El1D"
  }
  ~~~
  {: title="Response" }

---
This API call requires that you have first recieved an email containing an invitatation link. That link will contain an invitation token. Alternatively in a development environment, you may use the token included in the response to the (["Reset Password" API call](#organizationpassword-reset)).

This call will check to see if the token is valid. If the token is found, but has expired, a 201 response will be received and a new invitation email will be sent.

### URL Parameters:

token
: (string) The invitation token

### Response Parameters:

email
: (string) The email address to which the invitation belongs

token
: (string) The invitation token

### Expected Response Codes

| Code | Name      | Meaning                                      |
|------|----------------------------------------------------------|
| 200  | OK        | The token is valid                           |
| 201  | Created   | The token has expired. A new email was sent. |
| 404  | Not Found | The token is invalid                         |

{% include links/response_codes.md %}


~~~ bash
curl "http://localhost/organizations/accept-invite/KUMJLpo0tzFVeC5w1uni/"

~~~
{: title="Curl" }

~~~ bash
http GET 'http://localhost/organizations/accept-invite/KUMJLpo0tzFVeC5w1uni/'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Validate Invitation
    # GET http://localhost/organizations/accept-invite/KUMJLpo0tzFVeC5w1uni/

    try:
        response = requests.get(
            url="http://localhost/organizations/accept-invite/KUMJLpo0tzFVeC5w1uni/",
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
// request Validate Invitation
(function(callback) {
    'use strict';

    const httpTransport = require('http');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'localhost',
        port: '80',
        path: '/organizations/accept-invite/KUMJLpo0tzFVeC5w1uni/',
        method: 'GET',
        headers: {}
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
    request.write("")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
