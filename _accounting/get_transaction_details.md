---
title: /accounting/transactions/&lttransaction_id&gt/
name: Get Transaction Details
position: 1.1
method: get
description: Get Transaction Details for specific transactions
right_code: |
  ~~~ json
  {
    "statement_date": "2017-11-06",
    "payment_date": "2017-11-06",
    "transaction_id": "123456789",
    "total": "12.00",
    "status": "paid"
  }
  ~~~
  {: title="Response" }

---
Get the Transaction Details for a specific transaction on your account. The response includes details on the particular transaction_id you provide.

### Response Parameters:

statement_date
: (string) The Statement Date parameter is a date of when the statement was given

payment_date
: (string) The Payment Date parameter is a date of when the payment posted on the billing transaction

transaction_id
: (string) The Transaction Identifier parameter is an id number for the billing transaction

total
: (string) The Total parameter is the total amount on the billing transaction

status
: (string) The Status parameter is the status for the billing transaction

{% include links/response_codes.md %}

~~~ bash
curl "https://api-sandbox.cruxconnect.com/accounting/transactions/123456789/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d'

~~~
{: title="Curl" }

~~~ bash
http GET 'https://api-sandbox.cruxconnect.com/accounting/transactions/123456789/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Get Billing Transaction Details
    # GET https://api-sandbox.cruxconnect.com/accounting/transactions/123456789/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/accounting/transactions/123456789/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
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
// request Get Billing Transaction Details
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/accounting/transactions/123456789/',
        method: 'GET',
        headers: {"Authorization":"Token 47d4yfbwymedhiudj384702984nakju4hajh395d"}
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
