---
title: /api/notifications/notification-settings/
name: Get Notification Settings
position: 0.98
method: get
description: Get Notification Settings specific to your user account
right_code: |
  ~~~ json
  [
    {
      "uuid": "d72ffed5-6409-4c23-a88a-1f86043e8b0e",
      "notification_name": "Nearing Credit Limit",
      "notification_domain": "Billing",
      "notification_type": [
        {
          "notification_via": "Dashboard",
          "notification_frequency": "Daily",
          "enabled": true
        },
        {
          "notification_via": "email",
          "notification_frequency": "Daily",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "58506ba8-d0a7-4419-9bbe-f5d67371fac0",
      "notification_name": "Invoice Due",
      "notification_domain": "Billing",
      "notification_type": [
        {
          "notification_via": "Dashboard",
          "notification_frequency": "Daily",
          "enabled": false
        },
        {
          "notification_via": "email",
          "notification_frequency": "Daily",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "e944adff-5498-449c-9786-faec23b89cac",
      "notification_name": "Order Paid",
      "notification_domain": "Billing",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Twice a day",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    }
  ]
  ~~~
  {: title="Response" }

---
Get all the current Notification Settings specific to your user account. This returns the organization uuid, notification name, notification domain, notification type, annd more.

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Notification

notification_name
: (string) Notification Name is the name of the Notification you are receiving

notification_domain
: (string) Notification Domain is the domain to which the Notification pertains. Potential domains are "Billing", "Inventory", "Orders", and "Miscellaneous".

notification_type
: (list) Notification Type is a list with information about the Notifications you (will) receive including location, frequency, and if it is enabled.

org_user
: (object) Organization User is an object containing your user uuid

#### Notification Type Object:

notification_via
: (string) Notification Via indicates the location of the notification. Possible values are "Dashboard" and "email".

notification_frequency
: (string) Notification Frequency indicates the frequency of your notifications. Possible values include "Real-time", "Twice a day", and "Daily".

enabled
: (boolean) Enabled indicates if the Notification has been enabled for your account

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl "https://stable.projectthanos.com/api/notifications/notification-settings/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://stable.projectthanos.com/api/notifications/notification-settings/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Notification Settings
    # GET https://stable.projectthanos.com/api/notifications/notification-settings/

    try:
        response = requests.get(
            url="https://stable.projectthanos.com/api/notifications/notification-settings/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps()
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
// request Get Notification Settings
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/notifications/notification-settings/',
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
    request.write("{}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
