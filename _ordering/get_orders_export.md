---
title: /api/orders/export/
name: Get Orders Export
position: 3.01
method: post
description: Get an Export of the Orders via an email
right_code: |
  ~~~ json
  {
    "start": 0,
    "limit": 25,
    "sort": {
      "key": "uuid",
      "dir": "des"
    },
    "line_item_status": [
      "unallocated"
    ],
    "status_conjunction": "or",
    "start_date": "2017-07-31T06:00:00.000Z",
    "end_date": "2018-08-03T06:00:00.000Z"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "b9888421-594c-4d2f-9f0d-3b138a16c845"
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
: (array) One or more line item statuses. Will include orders with statuses based upon that `status_conjunction`. Possible Values are: `unallocated`, `allocated`, `rejected`, `has_tracking`, `backordered`

status_conjunction
: (string) Indicates how the line_item_status relates to the order response. Possible values are: `and`, `or`, `all`. Default: `or`. `And` will return all orders that have at least 1 line item matching each supplied status. `or` will return all orders that have at least one line item matching any of the supplied statuses. `only` will return orders that have ALL line items matching the supplied status. Only one line_item_status should be supplied when using `only`.

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
curl -X "POST" "https://api.cruxconnect.com/api/orders/export/" \
     -H 'Authorization: Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "sort": {
    "key": "uuid",
    "dir": "des"
  },
  "start": 0,
  "status_conjunction": "or",
  "start_date": "2017-07-31T06:00:00.000Z",
  "limit": 25,
  "line_item_status": [
    "unallocated"
  ],
  "end_date": "2018-08-03T06:00:00.000Z"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api.cruxconnect.com/api/orders/export/' \
    'Authorization':'Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c' \
    'Content-Type':'application/json; charset=utf-8' \
    sort:="{
  \"key\": \"uuid\",
  \"dir\": \"des\"
}" \
    start:=0 \
    status_conjunction="or" \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=25 \
    line_item_status:="[
  \"unallocated\"
]" \
    end_date="2018-08-03T06:00:00.000Z"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Orders Export
    # POST https://api.cruxconnect.com/api/orders/export/

    try:
        response = requests.post(
            url="https://api.cruxconnect.com/api/orders/export/",
            headers={
                "Authorization": "Token d7bb2fbb0c666dee5a5a36634baac3114e08ba9c",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    sort:="{
  \"key\": \"uuid\",
  \"dir\": \"des\"
}" \
    start:=0 \
    status_conjunction="or" \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=25 \
    line_item_status:="[
  \"unallocated\"
]" \
    end_date="2018-08-03T06:00:00.000Z")
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
        hostname: 'api.cruxconnect.com',
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
    request.write("{\"start\":0,\"limit\":25,\"sort\":{\"key\":\"uuid\",\"dir\":\"des\"},\"line_item_status\":[\"unallocated\"],\"status_conjunction\":\"or\",\"start_date\":\"2017-07-31T06:00:00.000Z\",\"end_date\":\"2018-08-03T06:00:00.000Z\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
