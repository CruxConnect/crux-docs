---
title: /timp/notifications/notification-settings/
name: Get Notification Settings
position: 2.12
visibility: public
method: get
description: Get Notification Settings specific to your user account
right_code: |
  ~~~ json
  [
    {
      "uuid": "d1b86ae6-8b70-41a0-afaa-1bc7d0bdec31",
      "notification_display_name": "Order Created",
      "notification_name": "orders/created",
      "notification_domain": "Orders",
      "notification_type": [],
      "org_user": null
    },
  ]
  ~~~
  {: title="Response" }

---
Get all the current Notification Settings specific to your user account. This returns the organization uuid, notification name, notification domain, notification type, annd more.

To view notification settings, you must be assigned the 'view_notifications_settings' permission
{: .info }


### Response Parameters:

uuid
: (string) Universal Unique Identifier for the Notification

notification_name
: (string) Notification Name is the name of the Notification you are receiving

notification_domain
: (string) Notification Domain is the domain to which the Notification pertains. Potential domains are "Billing", "Inventory", "Orders", and "Miscellaneous".

notification_type
: (array) Notification Type is a list with information about the Notifications you (will) receive including location, frequency, and if it is enabled.

org_user
: (object) Organization User is an object containing your user uuid

#### Notification Type Object:

notification_via
: (string) Notification Via indicates the location of the notification. Possible values are "Dashboard" and "email".

notification_frequency
: (string) Notification Frequency indicates the frequency of your notifications. Possible values include "Real-time", "Twice a day", and "Daily".

enabled
: (boolean) Enabled indicates if the Notification has been enabled for your account

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/timp/notifications/notification-settings/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/timp/notifications/notification-settings/' \
    'Authorization':'Token 1234567890' \
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
    # GET https://api-sandbox.cruxconnect.com/timp/notifications/notification-settings/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/timp/notifications/notification-settings/",
            headers={
                "Authorization": "Token 1234567890",
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
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/notifications/notification-settings/',
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
