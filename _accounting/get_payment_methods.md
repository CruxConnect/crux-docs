---
title: /accounting/payment-methods/
name: Get Payment Methods
position: 1.06
visibility: public
method: get
description: Get Payment Methods available on your account
right_code: |
  ~~~ json
  {
    "payment_type": "CREDIT CARD",
    "card_number": "4111111111111111",
    "card_last_four": "1111",
    "card_expiration": "2017-11-06",
    "is_default": true,
    "address": "1234 Crux Connect Way\nLehi, Utah 845005"
  }
  ~~~
  {: title="Response" }

---
Get Payment Methods available on your account. This returns the Payment Methods that are currently on your account. If you have removed any Payment Methods prior to this call, they will not appear in the list.

### Response Parameters:

payment_type
: (string) The Payment Type associated with the organization (e.g. "CREDIT CARD")

card_number
: (string) The 15 or 16 digit Card Number

card_last_four
: (string) The Last Four digits of your credit Card on file with your organization

card_expiration
: (string) The Card Expiration is the date in a YYYY-MM-DD format

is_default
: (boolean) The "Is Default" parameter indicates whether this is the default or not

address
: (string) The Address associated with the card

{% include links/response_codes.md %}

~~~ bash
curl "https://api-sandbox.cruxconnect.com/accounting/payment-methods/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/accounting/payment-methods/' \
    'Authorization':'Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
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
    # GET https://api-sandbox.cruxconnect.com/accounting/payment-methods/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/accounting/payment-methods/",
            headers={
                "Authorization": "Token 47d4yfbwymedhiudj384702984nakju4hajh395d",
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
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/accounting/payment-methods/',
        method: 'GET',
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
