---
title: /timp/products/catalogs/
name: Get Catalogs
position: 3.00
visibility: public
method: get
description: Get the Catalogs you have access to
right_code: |
  ~~~ json
  {
    "pagination": {
      "total_count": 150,
      "start": 30,
      "limit": 10,
    },
    "catalogs": [
      {
        "uuid": "f3603476-1f48-4ef9-a76c-0ec2f9c612fc",
        "supplier": {
          "uuid": "ed0eb521-1a0a-4526-a155-31daa726e66c"
        },
        "skus": [],
        "num_skus": 0,
        "default_shipping_cost": 5.33,
        "default_handling_cost": 1.89,
        "retailers": [],
        "created": "2018-08-24T01:00:53.219760Z",
        "last_updated": "2018-08-24T01:00:53.219813Z",
        "name": "Crux  Worldwide Connection QCSKlNstIhIpYPB1CKsh2H3ECh4ttVLD",
        "description": "Crux Worldwide Connection is a test catalog for the purposes of testing",
        "is_discoverable": null
      },
    ]
  }
  ~~~
  {: title="Response" }

---
Get the Catalogs you have access to.


### Response Parameters:

pagination
: (object) Pagination Object

catalogs
: (array) An array of Catalog objects

#### Pagination Object

{% include timp/product/response/pagination.md %}

#### Catalog Object

{% include timp/product/response/catalog.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-dev.cruxconnect.com/timp/products/catalogs/" \
     -H 'Authorization: Token a9e51a13fc4c02c5dcc02c3f41bf4f5fb9aa36ad'

~~~
{: title="Curl" }

~~~ bash
http GET 'https://api-dev.cruxconnect.com/timp/products/catalogs/' \
    'Authorization':'Token a9e51a13fc4c02c5dcc02c3f41bf4f5fb9aa36ad'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Get Catalogs
    # GET https://api-dev.cruxconnect.com/timp/products/catalogs/

    try:
        response = requests.get(
            url="https://api-dev.cruxconnect.com/timp/products/catalogs/",
            headers={
                "Authorization": "Token a9e51a13fc4c02c5dcc02c3f41bf4f5fb9aa36ad",
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
        hostname: 'api-dev.cruxconnect.com',
        port: '443',
        path: '/timp/products/catalogs/',
        method: 'GET',
        headers: {"Authorization":"Token a9e51a13fc4c02c5dcc02c3f41bf4f5fb9aa36ad"}
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
