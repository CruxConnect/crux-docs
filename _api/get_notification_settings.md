---
title: /api/notifications/notification-settings/
name: Get Notification Settings
position: 0.98
type: get
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
    },
    {
      "uuid": "ec6a5a45-3003-4455-b850-2c751ae91dae",
      "notification_name": "Late Invoice",
      "notification_domain": "Billing",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Real-time",
          "enabled": true
        },
        {
          "notification_via": "dashboard",
          "notification_frequency": "Daily",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "97215f89-c3dd-447e-8ab2-f7ded7a242f4",
      "notification_name": "Default Payment Method Changed",
      "notification_domain": "Billing",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Real-time",
          "enabled": true
        },
        {
          "notification_via": "dashboard",
          "notification_frequency": "Twice Daily",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "f5601368-62f7-4516-98b8-48785ba912e8",
      "notification_name": "Payment Method Added",
      "notification_domain": "Billing",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Real-time",
          "enabled": true
        },
        {
          "notification_via": "dashboard",
          "notification_frequency": "Daily",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "fa18db9f-6a22-4a62-a004-9692b34d104d",
      "notification_name": "Payment Method Removed",
      "notification_domain": "Billing",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Real-time",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "dee02e93-96fb-4cd8-8a26-a1b71d42fccd",
      "notification_name": "Low Inventory",
      "notification_domain": "Inventory",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Twice Daily",
          "enabled": true
        },
        {
          "notification_via": "dashboard",
          "notification_frequency": "Real Time",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "b575c5fc-2688-48c4-98ec-39e755029886",
      "notification_name": "Out of Stock",
      "notification_domain": "Inventory",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Twice a day",
          "enabled": true
        },
        {
          "notification_via": "dashboard",
          "notification_frequency": "Real Time",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "c2b061a0-2621-4c0a-bbdf-80e76fb9c632",
      "notification_name": "Price Change by %",
      "notification_domain": "Inventory",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Real-time",
          "enabled": true
        },
        {
          "notification_via": "dashboard",
          "notification_frequency": "Twice Daily",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "ecd50f40-1828-4f11-a7e2-e5156a14a09c",
      "notification_name": "Shipping Cost Change By %",
      "notification_domain": "Inventory",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Twice Daily",
          "enabled": true
        },
        {
          "notification_via": "dashboard",
          "notification_frequency": "Daily",
          "enabled": false
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "3db21acc-f03b-4f7f-af8c-0cab408c6e07",
      "notification_name": "Discontinued",
      "notification_domain": "Inventory",
      "notification_type": [
        {
          "notification_via": "Dashboard",
          "notification_frequency": "Twice Daily",
          "enabled": true
        },
        {
          "notification_via": "email",
          "notification_frequency": "Twice Daily",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "e2e14fd2-7e92-4f64-b4a8-a17bcea07102",
      "notification_name": "New Item in Product Feed",
      "notification_domain": "Inventory",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Twice Daily",
          "enabled": true
        },
        {
          "notification_via": "dashboard",
          "notification_frequency": "Daily",
          "enabled": false
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "a082ccf4-b581-4501-8395-fb62effe7516",
      "notification_name": "Deal Begins/Ends for Items in Inventory Lists",
      "notification_domain": "Inventory",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Real-time",
          "enabled": true
        },
        {
          "notification_via": "dashboard",
          "notification_frequency": "Real Time",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "b7de17ff-710a-4d6c-9092-221e8780c9a8",
      "notification_name": "Feed Update",
      "notification_domain": "Inventory",
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
      "uuid": "88947fa2-2455-4316-b93b-5dfa772a13ed",
      "notification_name": "Order Created",
      "notification_domain": "Orders",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Twice Daily",
          "enabled": true
        },
        {
          "notification_via": "dashboard",
          "notification_frequency": "Daily",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "f6d52426-d000-4510-bde0-bd3d7e8ebbb9",
      "notification_name": "Order Allocated",
      "notification_domain": "Orders",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Twice Daily",
          "enabled": true
        },
        {
          "notification_via": "dashboard",
          "notification_frequency": "Real Time",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "9786f30f-377d-487c-93a9-2e08f1a59112",
      "notification_name": "Order Tracking",
      "notification_domain": "Orders",
      "notification_type": [
        {
          "notification_via": "Dashboard",
          "notification_frequency": "Twice Daily",
          "enabled": true
        },
        {
          "notification_via": "email",
          "notification_frequency": "Twice Daily",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "0e4b2761-2618-40a7-9ccb-e725b85e6a7b",
      "notification_name": "Order Cancelled",
      "notification_domain": "Orders",
      "notification_type": [
        {
          "notification_via": "Dashboard",
          "notification_frequency": "Daily",
          "enabled": true
        },
        {
          "notification_via": "email",
          "notification_frequency": "Twice Daily",
          "enabled": true
        }
      ],
      "org_user": {
        "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
      }
    },
    {
      "uuid": "daf247dc-68c3-4ab8-93fc-024ae471bb91",
      "notification_name": "API Errors",
      "notification_domain": "Miscellaneous",
      "notification_type": [
        {
          "notification_via": "Email",
          "notification_frequency": "Real-time",
          "enabled": true
        },
        {
          "notification_via": "Dashboard",
          "notification_frequency": "Daily",
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
Get all the current Notification Settings specific to your user account. This returns the organization uuid, notification name, notification domain, notification type, annd more. Providing your username and password is optional as you can send your authorization token to receive this information.

URL Endpoint: /api/notifications/notification-settings/

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
