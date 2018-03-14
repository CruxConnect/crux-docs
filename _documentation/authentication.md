---
title: Authentication
position: 2
visibility: all
right_code: |
  ~~~ bash
  curl "https://api-sandbox.cruxconnect.com/path/to/api/endpoint/" \
    -H 'Authorization: Token YOUR_AUTH_TOKEN' \
    -H 'Content-Type: application/json; charset=utf-8' \
    -d $'{}'
  ~~~
  {: title="Curl" }

  ~~~ bash
  http --json GET 'https://api-sandbox.cruxconnect.com/path/to/api/endpoint/' \
    'Authorization':'Token YOUR_AUTH_TOKEN' \
    'Content-Type':'application/json; charset=utf-8'
  ~~~
  {: title="HTTPie" }

  ~~~ python
    # Install the Python Requests library:
    # `pip install requests`

    import requests
    import json


    def send_request():
        # Get All Permissions
        # GET https://api-sandbox.cruxconnect.com/path/to/api/endpoint/

        try:
            response = requests.get(
                url="https://api-sandbox.cruxconnect.com/path/to/api/endpoint/",
                headers={
                    "Authorization": "Token YOUR_AUTH_TOKEN",
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
    // request Get All Permissions
    (function(callback) {
        'use strict';

        const httpTransport = require('https');
        const responseEncoding = 'utf8';
        const httpOptions = {
            hostname: 'api-sandbox.cruxconnect.com',
            port: '443',
            path: '/path/to/api/endpoint/',
            method: 'GET',
            headers: {"Authorization":"Token YOUR_AUTH_TOKEN","Content-Type":"application/json; charset=utf-8"}
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
---

You need to be authenticated for all API requests. In order to get authenticated, you must first retreive your API token.
This can be done by <!--logging into to the UI and visiting account details, or --> sending a
[retreive auth token](#organizationretreive_auth_token) request.
The authentication token you receive is to be provided as a header in subsequent calls.

Add the auth_token as to calls as a header such as 'Authorization: Token \<auth_token\>'

You will experience errors if you do not include the authentication token. You may choose to also include your username
and password, although they are not required in subsequent calls.
