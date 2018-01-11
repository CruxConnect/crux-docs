---
title: /api/accounting/transactions/export/
name: Get Transactions Export
position: 1.4
type: post
description: Get Transactions Export allows you to receive an email with the current Transactions on your account
right_code: |
  ~~~ json
  {}
  ~~~
  {: title="Request" }


---
Get Transactions Export allows you to get an email with the Billing Transactions List. This API call, like other "Export" calls, will send an email to your email address. That is, the email address linked to your user_uuid. We also provide an Export uuid in response to this call.

### Response Parameters:

payment_date
: (string) Payment Date in the following format: YYYY-MM-DD

statement_date
: (string) Statement Date in the following format: YYYY-MM-DD

status
: (string) Status for the Transaction (e.g. "paid")

total
: (number) Total for the Transaction in USD (e.g. 29.95)

transaction_id
: (number) ID associated with the Transaction

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl -X "POST" "https://stable.projectthanos.com/api/accounting/transactions/export/" \
     -H 'Authorization: Token f97322af7ca5a5dacc73a6eae3e90dc975391fda' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://stable.projectthanos.com/api/accounting/transactions/export/' \
    'Authorization':'Token f97322af7ca5a5dacc73a6eae3e90dc975391fda' \
    'Content-Type':'application/json; charset=utf-8'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Billing Transactions Export
    # POST https://stable.projectthanos.com/api/accounting/transactions/export/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/accounting/transactions/export/",
            headers={
                "Authorization": "Token f97322af7ca5a5dacc73a6eae3e90dc975391fda",
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
// request Get Billing Transactions Export
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/accounting/transactions/export/',
        method: 'POST',
        headers: {"Authorization":"Token f97322af7ca5a5dacc73a6eae3e90dc975391fda","Content-Type":"application/json; charset=utf-8"}
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

