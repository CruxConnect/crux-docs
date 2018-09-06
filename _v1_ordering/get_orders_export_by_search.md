---
title: /orders/search/export/
name: Get Orders By Search
position: 5.03
visibility: v1
method: post
description: Get the Orders for your organization
right_code: |
  ~~~ json
  {
    "start": 0,
    "limit": 10,
    "line_item_allocation_statuses": [
      "Unallocated",
      "Partial",
      "Allocated"
    ],
    "line_item_designation": [],
    "term": "",
    "start_date": "2017-07-31T06:00:00.000Z",
    "end_date": "2018-08-03T06:00:00.000Z",
    "org_uuids": [],
    "sort": {
      "key": "date",
      "value": "asc"
    }
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "uuid": "9ff96aea-885c-4dc1-8a09-8e50fbe33119"
  }
  ~~~
  {: title="Response" }

---
Get Orders matching provided criteria for your organization sent to via email

This API call, like other “Export” calls, will send an email to your email address. That is, the email address linked to your user_uuid. The email will have a comma delimited file (.csv) attached with the response parameter data.

We also provide an array of the Export uuids in response to this call.


### Request Parameters:

#### Optional:

start
: (int) The Start is the number of which "Order" you would like to start. If no other filters are used, the default order, which is date created, is used. The default Start value is 0. If this filter is not included in your request, the default value is used.

limit
: (int) The Limit is the element number of "Order" in your Orders List where you would like your results to end. If you have 10 orders and you limit at 8 and start at 4, only orders 4, 5, 6, 7, and 8 are included in the results.


line_item_allocation_statuses
: (array) One or more line item statuses. Possible string values are: `Unallocated`, `Allocated`, `Partial`.

line_item_designation
: (array) One or more line item designations.  Possible string values are: `Rejected`, `HasTracking`, `Backordered`, `Cancelled`, `NeedsTracking`

term
: (string) Term can be Order UUID, PO Number or SKU ID

start_date
: (string) The Start Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

end_date
: (string) The End Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

sort
: (object) The Sort object contains a Key to sort on and a Direction (dir) to sort in

org_uuids
: (array) An array of Organization Universal Unique Identifiers

##### Sort Object:

key
: (string) The Key is the attribute on which you'd like to sort. Possible values include date, status, and sku_id.

dir
: (string) The Direction is ascending or descending entered as "asc" or "des"

### Response Parameters:

orders
: (array) The array of export uuids

### Expected Response Codes

Expected responses include 200, 400, 401, 403, or 404.


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/orders/search/export/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "org_uuids": [],
  "sort": {
    "key": "date",
    "value": "asc"
  },
  "start": 0,
  "start_date": "2017-07-31T06:00:00.000Z",
  "limit": 10,
  "line_item_designation": [],
  "line_item_allocation_statuses": [
    "Unallocated",
    "Partial",
    "Allocated"
  ],
  "end_date": "2018-08-03T06:00:00.000Z",
  "term": ""
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/orders/search/export/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8' \
    org_uuids:="[]" \
    sort:="{
  \"key\": \"date\",
  \"value\": \"asc\"
}" \
    start:=0 \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=10 \
    line_item_designation:="[]" \
    line_item_allocation_statuses:="[
  \"Unallocated\",
  \"Partial\",
  \"Allocated\"
]" \
    end_date="2018-08-03T06:00:00.000Z" \
    term=""

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Orders By Search
    # POST https://api-sandbox.cruxconnect.com/orders/search/export/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/orders/search/export/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    org_uuids:="[]" \
    sort:="{
  \"key\": \"date\",
  \"value\": \"asc\"
}" \
    start:=0 \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=10 \
    line_item_designation:="[]" \
    line_item_allocation_statuses:="[
  \"Unallocated\",
  \"Partial\",
  \"Allocated\"
]" \
    end_date="2018-08-03T06:00:00.000Z" \
    term="")
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
// request Get Orders By Search
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/orders/search/export/',
        method: 'POST',
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
    request.write("{\"start\":0,\"limit\":10,\"line_item_allocation_statuses\":[\"Unallocated\",\"Partial\",\"Allocated\"],\"line_item_designation\":[],\"term\":\"\",\"start_date\":\"2017-07-31T06:00:00.000Z\",\"end_date\":\"2018-08-03T06:00:00.000Z\",\"org_uuids\":[],\"sort\":{\"key\":\"date\",\"value\":\"asc\"}}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
