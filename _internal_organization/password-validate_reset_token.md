---
title: /organizations/complete-password/
name: Validate Password Token
position: 1.02
visibility: internal
method: get
description: Validate the password reset

---
This API call requires that you have first requested to reset your password (["Reset Password" API call](#organizationpassword-reset)). Validate that the password reset was requested on the email address provided. By sending a GET request with the email address an email is sent to you with the "reset token". That "reset token" can then be used with the "Complete Password Reset" API call. The reset token expires two hours after issuance.

### Request Parameters:

token
: (string) The reset token delivered to the email that was provided in the "Reset Password" API call

{% include links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/organizations/complete-password/?token=VBnQ8wmbEuJdoqpAFh01" \
     -H 'Content-Type: application/octet-stream'

~~~
{: title="Curl" }

~~~ bash
http GET 'https://api-sandbox.cruxconnect.com/organizations/complete-password/?token=VBnQ8wmbEuJdoqpAFh01' \
    'Content-Type':'application/octet-stream'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Validate Password Token
    # GET https://api-sandbox.cruxconnect.com/organizations/complete-password/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/organizations/complete-password/",
            params={
                "token": "VBnQ8wmbEuJdoqpAFh01",
            },
            headers={
                "Content-Type": "application/octet-stream",
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
// request Validate Password Token
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/organizations/complete-password/?token=VBnQ8wmbEuJdoqpAFh01',
        method: 'GET',
        headers: {"Content-Type":"application/octet-stream"}
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
