---
title: /accounting/transactions/
name: Get Transactions
position: 1.00
method: get
description: Get the Transactions for your account
right_code: |
  ~~~ json
  [
    {
      "statement_date": "2017-11-06",
      "payment_date": "2017-11-06",
      "transaction_id": "123456789",
      "total": "12.00",
      "status": "paid"
    },
    {
      "statement_date": "2017-11-06",
      "payment_date": "2017-11-06",
      "transaction_id": "456789101",
      "total": "10.99",
      "status": "paid"
    }
  ]
  ~~~
  {: title="Response" }

---
Get the Transactions for your account. This provides details for all billing transactions on your account.

### Response Parameters:

statement_date
: (string) The Statement Date parameter is a date of when the statement was given

payment_date
: (string) The Payment Date parameter is a date of when the payment posted on the billing transaction

transaction_id
: (string) The Transaction Identifier parameter is an id number for the billing transaction

total
: (number) The Total parameter is the total amount on the billing transaction

status
: (string) The Status parameter is the status for the billing transaction

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl "https:/.cruxconnect.com/accounting/transactions/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b'

~~~
{: title="Curl" }

~~~ bash
http GET 'https:/.cruxconnect.com/accounting/transactions/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Get Billing Transactions List
    # GET https:/.cruxconnect.com/accounting/transactions/

    try:
        response = requests.get(
            url="https:/.cruxconnect.com/accounting/transactions/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
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
// request Get Billing Transactions List
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api.cruxconnect.com',
        port: '443',
        path: '/accouting/transactions/',
        method: 'GET',
        headers: {"Authorization":"Token a0f17278bed479ee719ea890b8caf0329e1f3e5b"}
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
    request.write("")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }

