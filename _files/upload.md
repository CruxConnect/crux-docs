---
title: /organizations/files/upload/
name: Upload a File
position: 5.01
visibility: public
method: POST
description: Upload a file
---

For this request the the content-type header should be `multipart/form-data`.

### Request Parameters

file
: (string) The physical file to be uploaded.

filename
: (string) The filename for upload

### Response Parameters:

uuid
: (string) The Universal Unique Identifier for the uploaded file

### Expected Response Codes

{% include links/response_codes.md %}
