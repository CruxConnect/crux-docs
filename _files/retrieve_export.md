---
title: /api/data/export/&ltexport-uuid&gt/
name: Retrieve Export
position: 5.00
visibility: public
method: get
description: Retrieve a previously requested Export
right_code: |

  ~~~ json
  {
    "uuid": "d54c7721-0a6a-425c-b874-507437af3e11",
    "status": "COMPLETED",
    "url": "https://stable-exports.s3.amazonaws.com/order_export.csv?Signature=MN6L1KGTiicgitbbnXvJQLztpoU%3D&AWSAccessKeyId=AKIAID5FCZH4JE4B45XQ&Expires=1520954409"
  }
  ~~~
  {: title="Response" }

---
Retrieve a previously requested Export via the export_uuid. By calling this API Endpoint with the export_uuid in the URL, you can retrieve a previously requested Export.

Note: this endpoint does not include 'timp' in the path

### URL Parameters

export_uuid
: (string) The Universal Unique Identifier for the Export

### Response Parameters:

uuid
: (string) The Universal Unique Identifier for the Export

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/api/data/export/d54c7721-0a6a-425c-b874-507437af3e11/" \
     -H 'Authorization: Token 47d4yfbwymedhiudj384702984nakju4hajh395d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/api/data/export/d54c7721-0a6a-425c-b874-507437af3e11/' \
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
    # Retrieve Export
    # GET https://api-sandbox.cruxconnect.com/api/data/export/d54c7721-0a6a-425c-b874-507437af3e11/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/api/data/export/d54c7721-0a6a-425c-b874-507437af3e11/",
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
// request Retrieve Export
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/api/data/export/d54c7721-0a6a-425c-b874-507437af3e11/',
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
