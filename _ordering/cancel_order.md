---
title: /orders/cancel/
name: Cancel Order
position: 6.07
visibility: public
method: patch
description: Cancel a pending Order (for Retailers)
right_code: |
  ~~~ json
  {
    "order_uuid": "521a91e5-058d-4474-aeee-f0c148594a00"
  }
  ~~~
  {: title="Request" }


---
Cancel a pending Order. Granted that the supplier(s) can accept a cancellation, your request to cancel an order is sent to the pertinent supplier(s).


### Request Parameters:

order_uuid
: (string) The Universal Unique Identifier for the Order which you intend to cancel

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "PATCH" "https://api-dev.cruxconnect.com/orders/cancel/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "order_uuid": "521a91e5-058d-4474-aeee-f0c148594a00"
}'

~~~
{: title="Curl" }

~~~ bash
http --json PATCH 'https://api-dev.cruxconnect.com/orders/cancel/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    order_uuid="521a91e5-058d-4474-aeee-f0c148594a00"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Cancel Order
    # PATCH https://api-dev.cruxconnect.com/orders/cancel/

    try:
        response = requests.patch(
            url="https://api-dev.cruxconnect.com/orders/cancel/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    order_uuid="521a91e5-058d-4474-aeee-f0c148594a00")
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
// request Cancel Order 
(function(callback) {
    'use strict';
        
    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/orders/cancel/',
        method: 'PATCH',
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
    request.write("{\"order_uuid\":\"521a91e5-058d-4474-aeee-f0c148594a00\"}")
    request.end();
    

})((error, statusCode, headers, body) => {
    console.log('ERROR:', error); 
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
