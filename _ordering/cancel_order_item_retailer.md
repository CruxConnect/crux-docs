---
title: /orders/items/cancel/&ltorder_item_uuid&gt/
name: Cancel Order Item - Retailer
position: 3.07
method: delete
description: Cancel an item on a pending Order (for Retailers)
right_code: |

---
Cancel a pending Order. Granted that the supplier(s) can accept a cancellation, your request to cancel an order is sent to the pertinent supplier(s).


| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 204  | No Content             | The API call was received and the order cancel request is now pending        |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |
| 422  | Unprocessable Entity   | Generally, the order_item_uuid can't be cancelled or may be wrong altogether |


~~~ bash
curl -X "DELETE" "https:/.cruxconnect.com/orders/items/cancel//" \
     -H 'Authorization: Token 825dd305b5858e2373763ff338615db822fe67a0' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json DELETE 'https:/.cruxconnect.com/orders/items/cancel//' \
    'Authorization':'Token 825dd305b5858e2373763ff338615db822fe67a0' \
    'Content-Type':'application/json; charset=utf-8'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Cancel Order Item - Retailer
    # DELETE https:/.cruxconnect.com/orders/items/cancel//

    try:
        response = requests.delete(
            url="https:/.cruxconnect.com/orders/items/cancel//",
            headers={
                "Authorization": "Token 825dd305b5858e2373763ff338615db822fe67a0",
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
// request Cancel Order Item - Retailer
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api.cruxconnect.com',
        port: '443',
        path: '/orders/items/cancel//',
        method: 'DELETE',
        headers: {"Authorization":"Token 825dd305b5858e2373763ff338615db822fe67a0","Content-Type":"application/json; charset=utf-8"}
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
