---
title: /api/orders/export/
name: Get Orders Export
position: 3.01
type: post
description: Get an Export of the Orders via an email
right_code: |
  ~~~ json
  {}
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "eea176f9-f31c-4064-8ef6-0851264c6ee4"
  }
  ~~~
  {: title="Response" }

---
Get an Export of the Orders via an email to your email address on file. This API call, like other "Export" calls, will send an email to your email address. That is, the email address linked to your user_uuid. We also provide an Export uuid in response to this call.

### Request Parameters:

#### Optional:

start
: (number) The Start is the number of which "Order" you would like to start. If no other filters are used, the default order, which is date created, is used. The default Start value is 0. If this filter is not included in your request, the default value is used.

limit
: (number) The Limit is the element number of "Order" in your Orders List where you would like your results to end. If you have 10 orders and you limit at 8 and start at 4, only orders 4, 5, 6, 7, and 8 are included in the results.

sort
: (object) The Sort object contains a Key to sort on and a Direction (dir) to sort in

line_item_status
: (string) The Status for the Line Item. These can be "unallocated", "allocated", "rejected", "has_tracking", "backordered", and "delivered". The Status of the Line Items within orders you would like to see returned.

start_date
: (string) The Start Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

end_date
: (string) The End Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

### Response Parameters:

uuid
: (string) The Universal Unique Identifier for the Export

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl -X "POST" "https://stable.projectthanos.com/api/orders/export/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "limit": 25,
  "end_date": "2018-08-03T06:00:00.000Z",
  "line_item_status": "unallocated",
  "sort": {
    "key": "uuid",
    "dir": "des"
  },
  "start_date": "2017-07-31T06:00:00.000Z",
  "start": 0
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://stable.projectthanos.com/api/orders/export/' \
    'Authorization':'Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c' \
    'Content-Type':'application/json; charset=utf-8' \
    limit:=25 \
    end_date="2018-08-03T06:00:00.000Z" \
    line_item_status="unallocated" \
    sort:="{
  \"key\": \"uuid\",
  \"dir\": \"des\"
}" \
    start_date="2017-07-31T06:00:00.000Z" \
    start:=0

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Orders Export
    # POST https://stable.projectthanos.com/api/orders/export/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/orders/export/",
            headers={
                "Authorization": "Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps({
                "limit": 25,
                "end_date": "2018-08-03T06:00:00.000Z",
                "line_item_status": "unallocated",
                "sort": {
                    "key": "uuid",
                    "dir": "des"
                },
                "start_date": "2017-07-31T06:00:00.000Z",
                "start": 0
            })
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
// request Get Orders Export
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/orders/export/',
        method: 'POST',
        headers: {"Authorization":"Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"start\":0,\"limit\":25,\"sort\":{\"key\":\"uuid\",\"dir\":\"des\"},\"line_item_status\":\"unallocated\",\"start_date\":\"2017-07-31T06:00:00.000Z\",\"end_date\":\"2018-08-03T06:00:00.000Z\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
