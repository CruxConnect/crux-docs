---
title: /timp/products/catalogs/
name: Get Catalogs
position: 3.00
visibility: public
method: get
description: Get the Catalogs you have access to
right_code: |
  ~~~ json

  ~~~
  {: title="Request" }

  ~~~ json
  []
  ~~~
  {: title="Response" }

---
Get the Catalogs you have access to.


### Response Parameters:

An array of catalog objects is returned

### Catalog Object

{% include timp/product/response/catalog.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/timp/products/catalogs/" \
     -H 'Authorization: Token 1234567890'

~~~
{: title="Curl" }

~~~ bash
http GET 'https://api-sandbox.cruxconnect.com/timp/products/catalogs/' \
    'Authorization':'Token 1234567890'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Get Catalogs
    # GET https://api-sandbox.cruxconnect.com/timp/products/catalogs/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/timp/products/catalogs/",
            headers={
                "Authorization": "Token 1234567890",
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
// request Get Catalogs
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/products/catalogs/',
        method: 'GET',
        headers: {"Authorization":"Token 1234567890"}
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
