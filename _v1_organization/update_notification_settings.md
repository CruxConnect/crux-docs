---
title: /notifications/notification-settings/
name: Update Notification Settings
position: 1.14
visibility: v1
method: put
description: Update Notification Settings allows you to update a single notification's settings
right_code: |
  ~~~ json
  {
    "notification_via": "Dashboard",
    "enabled": "True",
    "notification_frequency": "Daily",
    "uuid": "daf247dc-68c3-4ab8-93fc-024ae471bb91"
  }
  ~~~
  {: title="Request" }


---
Update Notification Settings allows you to update a single Notification's settings. By providing the uuid for the notification with the location, frequency, and "enabled" you may update a Notification.

To view notification settings, you must be assigned the 'view_notifications_settings' permission
{: .info }

To edit email notification preferences, you must be assigned the 'edit_email_notifications_preferences' permission
{: .info }

### Request Parameters:

uuid
: (string) The Universal Unique Identifier for the Notification

notification_via
: (string) The Notification Via parameter refers to the location where you'll receive the Notification, either "Dashboard" or "email"

enabled
: (boolean) The Enabled parameter refers to whether this is available to the user

notification_frequency
: (string) The Notification Frequency refers to how often you'll be notified. Possible values are "Real-time", "Twice a day", and "Daily"

{% include v1/links/response_codes.md %}

~~~ bash
curl -X "PUT" "https://api-sandbox.cruxconnect.com/notifications/notification-settings/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "notification_via": "Dashboard",
  "enabled": "True",
  "notification_frequency": "Daily",
  "uuid": "daf247dc-68c3-4ab8-93fc-024ae471bb91"
}'

~~~
{: title="Curl" }

~~~ bash
http --json PUT 'https://api-sandbox.cruxconnect.com/notifications/notification-settings/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
    'Content-Type':'application/json; charset=utf-8' \
    notification_via="Dashboard" \
    enabled="True" \
    notification_frequency="Daily" \
    uuid="daf247dc-68c3-4ab8-93fc-024ae471bb91"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Update Notification Settings
    # PUT https://api-sandbox.cruxconnect.com/notifications/notification-settings/

    try:
        response = requests.put(
            url="https://api-sandbox.cruxconnect.com/notifications/notification-settings/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    notification_via="Dashboard" \
    enabled="True" \
    notification_frequency="Daily" \
    uuid="daf247dc-68c3-4ab8-93fc-024ae471bb91")
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
// request Update Notification Settings
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/notifications/notification-settings/',
        method: 'PUT',
        headers: {"Authorization":"Token 47d4yfbwymedhiudj384702984nakju4hajh395d","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"notification_via\":\"Dashboard\",\"enabled\":\"True\",\"notification_frequency\":\"Daily\",\"uuid\":\"daf247dc-68c3-4ab8-93fc-024ae471bb91\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
