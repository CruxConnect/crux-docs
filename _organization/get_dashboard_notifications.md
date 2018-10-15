---
title: /timp/notifications/
name: Get Dashboard Notifications
position: 2.11
visibility: public
method: get
description: Get the Dashboard Notifications for your account
right_code: |
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

To view orders, you must be assigned the 'view_orders' permission
{: .info }

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Notification

title
: (string) The Title for the Notification

created_at
: (string) The Created At parameter indicates the date and timestamp of when the Notification was created

type
: (string) The Type parameter indicates where the notification is sent. For this call it should always say "Dashboard".

{% include timp/links/response_codes.md %}

~~~ bash
curl "https://api-sandbox.cruxconnect.com/timp/notifications/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "user_uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/timp/notifications/' \
    'Authorization':'Token 1234567890' \
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
    # GET https://api-sandbox.cruxconnect.com/timp/notifications/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/timp/notifications/",
            headers={
                "Authorization": "Token 1234567890",
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
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/notifications/',
        method: 'GET',
        headers: {"Authorization":"Token 1234567890","Content-Type":"application/json; charset=utf-8"}
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
