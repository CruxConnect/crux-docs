---
title: /accounting/transactions/export/
name: Get Transactions Export
position: 1.4
visibility: public
method: post
description: Get Transactions Export allows you to receive an email with the current Transactions on your account
right_code: |
  ~~~ json
  {
    "uuid": "r5682624-3167-47d2-8b09-3cdf3c1fd61b"
  }
  ~~~
  {: title="Response" }


---
Get Transactions Export allows you to get an email with the Billing Transactions List.

This API call, like other "Export" calls, will send an email to your email address. That is, the email address linked to your user_uuid. The email will have a comma delimited file (.csv) attached with the response parameter data.

We also provide an Export uuid in response to this call.

### Response Parameters:

payment_date
: (string) Payment Date in the following format: YYYY-MM-DD

statement_date
: (string) Statement Date in the following format: YYYY-MM-DD

status
: (string) Status for the Transaction (e.g. "paid")

total
: (string) Total for the Transaction in USD (e.g. 29.95)

transaction_id
: (string) ID associated with the Transaction

{% include links/response_codes.md %}

~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/accounting/transactions/export/" \
     -H 'Authorization: Token f97322af7ca5a5dacc73a6eae3e90dc975391fda' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/accounting/transactions/export/' \
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
    # POST https://api-sandbox.cruxconnect.com/accounting/transactions/export/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/accounting/transactions/export/",
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
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/accounting/transactions/export/',
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

