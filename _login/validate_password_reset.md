---
title: /api/organizations/complete-password/
name: Validate Password Reset
position: 0.2
type: get
description: Validate the password reset
right_code: |
  ~~~ json
  {
    "email": "jweir@projectthanos.com"
  }
  ~~~
  {: title="Request" }


---
This API call requires that you have first requested to reset your password ("Reset Password" API call). Validate that the password reset was requested on the email address provided. By sending a GET request with the email address an email is sent to you with the "reset token". That "reset token" can then be used with the "Complete Password Reset" API call

### Request Parameters:

email
: (string) The email you provided in your "Reset Password" API call

| Code | Name                   | Meaning                                                                                  |
|------|------------------------|------------------------------------------------------------------------------------------|
| 204  | No Content             | The API call was received and an email was sent to the email address provided            |
| 404  | Not Found              | Generally, the call is not sent to the correct URL or email address is not in our system |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                                      |


~~~ bash
curl "https://stable.projectthanos.com/api/organizations/complete-password/?token=G7TwCq1Vkds0DLYnfAuP" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: text/plain; charset=utf-8' \
     -d $'{
  "email": "jweir@projectthanos.com"
}'

~~~
{: title="Curl" }

~~~ bash
http --form GET 'https://stable.projectthanos.com/api/organizations/complete-password/?token=G7TwCq1Vkds0DLYnfAuP' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'text/plain; charset=utf-8' \
    'data'=$'{
  \"email\": \"jweir@projectthanos.com\"
}'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Validate Password Reset
    # GET https://stable.projectthanos.com/api/organizations/complete-password/

    try:
        response = requests.get(
            url="https://stable.projectthanos.com/api/organizations/complete-password/",
            params={
                "token": "G7TwCq1Vkds0DLYnfAuP",
            },
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
// request Validate Password Reset
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/organizations/complete-password/?token=G7TwCq1Vkds0DLYnfAuP',
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
    request.write("{\n  \"email\": \"jweir@projectthanos.com\"\n}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
