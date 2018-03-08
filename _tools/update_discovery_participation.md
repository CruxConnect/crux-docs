---
title: /catalog/update
name: Update Discovery Participation
visibility: internal
position: 5.10
method: post
description: Update Discovery Catalog Participation
right_code: |
  ~~~ json
  {
    "supplier_uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
    "participation": true,
    "discovery_catalog_uuid": "05a46c58-9d13-4912-9167-7effc2cc7482"
  }
  ~~~
  {: title="Request" }

---
Update Supplier participation in the Discovery Catalog and the identify which catalog they will use as their Discovery Catalog

### Request

supplier_uuid
: (string) The Universal Unique Identifier for the Supplier

participation
: (bool) Whether or not the Supplier will participate in Discovery Catalog

discovery_catalog_uuid
: (string) The Universal Unique Identifier for the Discovery Catalog. Required if participation is true.  Empty/Ignored if not participating.

#### Response

200 Success

~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/catalog/update" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "": ""
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/catalog/update' \
    'Content-Type':'application/json; charset=utf-8' \
    =""

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Update Discovery Participation and Catalog
    # POST https://api-sandbox.cruxconnect.com/catalog/update

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/catalog/update",
            headers={
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    ="")
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
// request Update Discovery Participation and Catalog
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/catalog/update',
        method: 'POST',
        headers: {"Content-Type":"application/json; charset=utf-8"}
    };
    httpOptions.headers['User-Agent'] = 'node ' + process.version;

    // Paw Store Cookies option is not supported

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
    request.write("{\"\":\"\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }