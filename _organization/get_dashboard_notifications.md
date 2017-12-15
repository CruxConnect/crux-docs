---
title: /api/notifications/
name: Get Dashboard Notifications
position: 0.96
type: get
description: Get the Dashboard Notifications for your account
right_code: |
  ~~~ json
  {
    "user_uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  [
    {
      "uuid": "ed059353-71d6-44da-a676-22134e37bcc4",
      "title": "API Errors",
      "created_at": "2017-11-06T20:41:02.497923Z",
      "type": "Dashboard"
    }
  ]
  ~~~
  {: title="Response" }

---
Get the Dashboard Notificationas for your account. These are all of the enabled notifications that you are receiving on your Dashboard.

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Notification

title
: (string) The Title for the Notification

created_at
: (string) The Created At parameter indicates the date and timestamp of when the Notification was created

type
: (string) The Type parameter indicates where the notification is sent. For this call it should always say "Dashboard".

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl "https://stable.projectthanos.com/api/notifications/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "user_uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://stable.projectthanos.com/api/notifications/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8' \
    user_uuid="3a7acb28-ab13-437e-8c35-46cf4f0bea49"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Dashboard Notifications
    # GET https://stable.projectthanos.com/api/notifications/

    try:
        response = requests.get(
            url="https://stable.projectthanos.com/api/notifications/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    user_uuid="3a7acb28-ab13-437e-8c35-46cf4f0bea49")
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
// request Get Dashboard Notifications
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/notifications/',
        method: 'GET',
        headers: {"Authorization":"Token a0f17278bed479ee719ea890b8caf0329e1f3e5b","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"user_uuid\":\"3a7acb28-ab13-437e-8c35-46cf4f0bea49\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
