---
title: /organizations/files/upload/
name: Upload a File
position: 5.01
visibility: public
method: PUT
description: Upload a file
---

For this request the the content-type header should be `multipart/form-data`.

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
