---
title: /api/orders/&ltorder_uuid&gt/export/
name: Get Order Detail Export
position: 3.03
method: post
description: Get an Export of an Order with Details via an email.
right_code: |
  ~~~ json
  {
    "order_uuid": "bce99b67-2b23-43b8-a229-9c97b9e79935"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "232497cc-95eb-4ffd-a084-edea0c413267"
  }
  ~~~
  {: title="Response" }

---
Get an Export of an Order with Details via an email to your email address on file. This API call, like other "Export" calls, will send an email to your email address. That is, the email address linked to your user_uuid.

### Response Parameters:

uuid
: (string) The Universal Unique Identifier for the Export

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl -X "POST" "https://api.cruxconnect.com/api/orders/299fc593-04f0-424d-9847-e359b9dfde56/export/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "order_uuid": "bce99b67-2b23-43b8-a229-9c97b9e79935"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api.cruxconnect.com/api/orders/299fc593-04f0-424d-9847-e359b9dfde56/export/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8' \
    order_uuid="bce99b67-2b23-43b8-a229-9c97b9e79935"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Order Detail Export
    # POST https://api.cruxconnect.com/api/orders/299fc593-04f0-424d-9847-e359b9dfde56/export/

    try:
        response = requests.post(
            url="https://api.cruxconnect.com/api/orders/299fc593-04f0-424d-9847-e359b9dfde56/export/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    order_uuid="bce99b67-2b23-43b8-a229-9c97b9e79935")
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
// request Get Order Detail Export
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api.cruxconnect.com',
        port: '443',
        path: '/api/orders/299fc593-04f0-424d-9847-e359b9dfde56/export/',
        method: 'POST',
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
    request.write("{\"order_uuid\":\"bce99b67-2b23-43b8-a229-9c97b9e79935\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
