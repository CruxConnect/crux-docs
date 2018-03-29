---
title: /discovery/participation/&lt;org_uuid&gt;/
name: Get Discovery Participation
visibility: internal
position: 5.20
method: get
description: Get Discovery Catalog Participation
right_code: |
  ~~~ json
    {
      "supplier_uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
      "is_participating": true,
      "discovery_catalog_uuid": "05a46c58-9d13-4912-9167-7effc2cc7482"
    }
  ~~~
  {: title="Response" }

---
Get Supplier participation in the Discovery Catalog and, if participating, the catalog the Supplier will use as their Discovery Catalog

### Request
supplier_uuid
: (uuid) The Universal Unique Identifier for the Supplier

### Response

supplier_uuid
: (string) The Universal Unique Identifier for the Supplier

is_participating
: (bool) Whether or not the Supplier will participate in Discovery Catalog

discovery_catalog_uuid
: (string) The Universal Unique Identifier for the Discovery Catalog. Empty if not participating.

~~~ bash
curl "https://api-dev.cruxconnect.com/catalog/&ltuuid&gt/"

~~~
{: title="Curl" }

~~~ bash
http GET 'https://api-dev.cruxconnect.com/catalog/&ltuuid&gt/'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Get Discovery Participation
    # GET https://api-dev.cruxconnect.com/catalog/&ltuuid&gt/

    try:
        response = requests.get(
            url="https://api-dev.cruxconnect.com/catalog/&ltuuid&gt/",
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
// request Get Discovery Participation
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/catalog/&ltuuid&gt/',
        method: 'GET',
        headers: {}
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
