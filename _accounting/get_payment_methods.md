---
title: /api/accounting/payment-methods/
name: Get Payment Methods
position: 1.3
type: get
description: Get Payment Methods available on your account
right_code: |
  ~~~ json
  {
    "payment_type": "CREDIT CARD",
    "card_number": "4111111111111111",
    "card_last_four": "1111",
    "card_expiration": "2017-11-06",
    "is_default": true,
    "address": "1234 Thanos Road\nLehi, Utah 845005"
  }
  ~~~
  {: title="Response" }

---
Get Payment Methods available on your account. This returns the Payment Methods that are currently on your account. If you have removed any Payment Methods prior to this call, they will not appear in the list. Your username and password are optional as you can send your authorization token to receive this information.

### Response Parameters:

payment_type
: (string) The Payment Type associated with the organization (e.g. "CREDIT CARD")

card_number
: (number) The 15 or 16 digit Card Number

card_last_four
: (number) The Last Four digits of your credit Card on file with your organization

card_expiration
: (string) The Card Expiration is the date in a YYYY-MM-DD format

is_default
: (boolean) The "Is Default" parameter indicates whether this is the default or not

address
: (string) The Address assocated with the card

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl "https://stable.projectthanos.com/api/accounting/payment-methods/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://stable.projectthanos.com/api/accounting/payment-methods/' \
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
    # Get Payment Methods
    # GET https://stable.projectthanos.com/api/accounting/payment-methods/

    try:
        response = requests.get(
            url="https://stable.projectthanos.com/api/accounting/payment-methods/",
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
// request Get Payment Methods
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/accounting/payment-methods/',
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
