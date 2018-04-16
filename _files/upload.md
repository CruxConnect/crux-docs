---
title: /organizations/files/upload/
name: Upload a File
position: 9.00
visibility: public
method: post
description: Upload A File
right_code: |
  ~~~ json
  {
    "filename": "My File"
    "file": "File contents in a multipart/form-data format"
  }
  ~~~
  {: title="Request" }
  ~~~ json
  {
    "uuid": "70f0fc07-23ef-4174-ac67-def3c629b7ea"
  }
  ~~~
  {: title="Response" }

---
Upload a File

For this request the the content-type header should be `multipart/form-data`.

### Request Parameters

{% include objects/file_upload.md %}

### Response Parameters:

uuid
: (string) The Universal Unique Identifier for the uploaded file. (For clarity: the UUID goes with the upload, not the file. If you upload the exact same file more than once, each upload will have its own UUID.)

### Expected Response Codes

{% include links/response_codes.md %}

### Expected Response Codes

# Short Description
Upload A File

# Long Description
Upload a File

For this request the content-type header should be `multipart/form-data`.

### Request Parameters

file
: (string) The file contents for upload

filename
: (string) The filename for upload

### Response Parameters:

uuid
: (string) The Universal Unique Identifier for the uploaded file

### Expected Response Codes

{% include links/response_codes.md %}


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/organizations/files/upload/" \
     -H 'Cookie: sessionid=6tkaww9xmbj4d3fnw89zp4hewosvb94u' \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: multipart/form-data; charset=utf-8; boundary=__X_PAW_BOUNDARY__' \
     -F "filename=myfile" \
     -F "file={\\rtf1\\ansi\\ansicpg1252\\cocoartf1561\\cocoasubrtf400
{\\fonttbl\\f0\\fswiss\\fcharset0 Helvetica;}
{\\colortbl;\\red255\\green255\\blue255;}
{\\*\\expandedcolortbl;;}
\\margl1440\\margr1440\\vieww21600\\viewh8400\\viewkind0
\\pard\\tx720\\tx1440\\tx2160\\tx2880\\tx3600\\tx4320\\tx5040\\tx5760\\tx6480\\tx7200\\tx7920\\tx8640\\pardirnatural\\partightenfactor0

\\f0\\fs24 \\cf0 My File contents}"

~~~
{: title="Curl" }

~~~ bash
# note: HTTPie will post as form url-encoded if no file is specified
http --form POST 'https://api-sandbox.cruxconnect.com/organizations/files/upload/' \
    'Cookie':'sessionid=6tkaww9xmbj4d3fnw89zp4hewosvb94u' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'multipart/form-data; charset=utf-8; boundary=__X_PAW_BOUNDARY__' \
    'filename'='myfile' \
    'file'='{\\rtf1\\ansi\\ansicpg1252\\cocoartf1561\\cocoasubrtf400
{\\fonttbl\\f0\\fswiss\\fcharset0 Helvetica;}
{\\colortbl;\\red255\\green255\\blue255;}
{\\*\\expandedcolortbl;;}
\\margl1440\\margr1440\\vieww21600\\viewh8400\\viewkind0
\\pard\\tx720\\tx1440\\tx2160\\tx2880\\tx3600\\tx4320\\tx5040\\tx5760\\tx6480\\tx7200\\tx7920\\tx8640\\pardirnatural\\partightenfactor0

\\f0\\fs24 \\cf0 My File contents}'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Upload a File
    # POST https://api-sandbox.cruxconnect.com/organizations/files/upload/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/organizations/files/upload/",
            headers={
                "Cookie": "sessionid=6tkaww9xmbj4d3fnw89zp4hewosvb94u",
                "Authorization": "Token 1234567890",
                "Content-Type": "multipart/form-data; charset=utf-8; boundary=__X_PAW_BOUNDARY__",
            },
            files={
                "filename": "myfile",
                "file": "{\\rtf1\\ansi\\ansicpg1252\\cocoartf1561\\cocoasubrtf400
{\\fonttbl\\f0\\fswiss\\fcharset0 Helvetica;}
{\\colortbl;\\red255\\green255\\blue255;}
{\\*\\expandedcolortbl;;}
\\margl1440\\margr1440\\vieww21600\\viewh8400\\viewkind0
\\pard\\tx720\\tx1440\\tx2160\\tx2880\\tx3600\\tx4320\\tx5040\\tx5760\\tx6480\\tx7200\\tx7920\\tx8640\\pardirnatural\\partightenfactor0

\\f0\\fs24 \\cf0 My File contents}",
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
// request Upload a File
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/organizations/files/upload/',
        method: 'POST',
        headers: {"Cookie":"sessionid=6tkaww9xmbj4d3fnw89zp4hewosvb94u","Authorization":"Token 1234567890","Content-Type":"multipart/form-data; charset=utf-8; boundary=__X_PAW_BOUNDARY__"}
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
    request.write("--__X_PAW_BOUNDARY__\r\nContent-Disposition: form-data; name=\"filename\"\r\n\r\nmyfile\r\n--__X_PAW_BOUNDARY__\r\nContent-Disposition: form-data; name=\"file\"; filename=\"MyFile.rtf\"\r\nContent-Type: text/rtf\r\n\r\n{\\rtf1\\ansi\\ansicpg1252\\cocoartf1561\\cocoasubrtf400\n{\\fonttbl\\f0\\fswiss\\fcharset0 Helvetica;}\n{\\colortbl;\\red255\\green255\\blue255;}\n{\\*\\expandedcolortbl;;}\n\\margl1440\\margr1440\\vieww21600\\viewh8400\\viewkind0\n\\pard\\tx720\\tx1440\\tx2160\\tx2880\\tx3600\\tx4320\\tx5040\\tx5760\\tx6480\\tx7200\\tx7920\\tx8640\\pardirnatural\\partightenfactor0\n\n\\f0\\fs24 \\cf0 My File contents}\r\n--__X_PAW_BOUNDARY__--\r\n")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
