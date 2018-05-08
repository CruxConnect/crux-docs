---
title: /products/catalogs/
name: Get Catalogs
position: 4.0
visibility: public
method: get
description: Get the Catalogs you have access to
right_code: |
  ~~~ json
  [
    {
      "uuid": "38504ca3-27ea-4478-85a2-25f01cde1652",
      "supplier": {
        "uuid": "86ab12cd-fd66-4122-8b81-f837bc72d755"
      },
      "skus": [
        {
          "uuid": "bb479ac7-4dd9-4411-a6e9-a265e51aa434"
        },
        {
          "uuid": "95848455-d19b-48f8-8f53-5791818ddeca"
        },
      ],
      "num_skus": 30,
      "default_shipping_cost": null,
      "default_handling_cost": null,
      "retailer": {
        "uuid": "7c8ceed8-86c3-4c4f-9b45-8bda5aa665b2"
      },
      "created": "2018-04-06T01:12:09.804995Z",
      "last_updated": "2018-04-06T01:12:18.259897Z",
      "name": "The elfin industry catalog",
      "description": "Because if your elfin industry catalog is bold, incomplete, and beautiful, everyone will think that of your believe, too! It's clear, crisp, and guaranteed! Oh, no you don't!  Our elfin industry catalog kicks the earthy competition in the smile! Because we care about how your elfin industry catalog looks! You know what's accurate about elfin industry catalog? Because without elfin industry catalog, you would look so cheery, don't you think? Be the kind of person your mother wanted you to me. All your wildest dreams would come true. All the other kids with the pumped up kicks will wish they had elfin industry catalog. I like, it, I love it, I want some more of it. When it's all said and done, there's still elfin industry catalog. Still. You know you want it."
    },
    {
      "uuid": "8a934ceb-d0f7-45e3-94b9-ae6e43fc6168",
      "supplier": {
        "uuid": "88971331-5e51-47be-a762-536499ad0366"
      },
      "skus": [
        {
          "uuid": "3e35bc21-ddd3-4b27-99b8-551dfb92d305"
        }
      ],
      "num_skus": 1,
      "default_shipping_cost": null,
      "default_handling_cost": null,
      "retailer": {
        "uuid": "7c8ceed8-86c3-4c4f-9b45-8bda5aa665b2"
      },
      "created": "2018-04-06T01:12:17.882097Z",
      "last_updated": "2018-04-06T01:12:17.882153Z",
      "name": "The chubby insurance catalog",
      "description": "Because we care about how your chubby insurance catalog looks! And then there's our chubby insurance catalog, which will blow off your chunky pig!! There's just something chemical about cuddling up with your own chubby insurance catalog! When it's all said and done, there's still chubby insurance catalog. Still. It's clear, crisp, and guaranteed! chubby insurance catalog works best when you give it plenty of TLC. You know what's impure about chubby insurance catalog? Be the hero. Oh, no you don't!  Our chubby insurance catalog kicks the chunky competition in the rice! Our chubby insurance catalog comes with built-in basin for that extra innocent flavor."
    }
  ]
  ~~~
  {: title="Response" }

---
Get the Catalogs you have access to.


### Response Parameters:

An array of catalog objects is returned

### Catalog Object

{% include product/response/catalog.md %}

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/products/catalogs/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/products/catalogs/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Catalogs
    # GET https://api-sandbox.cruxconnect.com/products/catalogs/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/products/catalogs/",
            headers={
                "Authorization": "Token 1234567890",
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
// request Get Catalogs
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/products/catalogs/',
        method: 'GET',
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
