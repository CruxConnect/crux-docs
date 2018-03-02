---
title: Response Codes
position: 4
---

Expected response that you might see returned.  If there is an additional response code that might occur, we'll identify it in the associated document.

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 201  | Created                | The API call was received and something was created                          |
| 204  | No Content             | The API call was received and we are performing the requested action         |
| 400  | Bad Request            | Something required for the request is missing                                |
| 401  | Unauthorized           | The authentication credentials (username/password or token) are incorrect.   |
| 403  | Permission Denied      | The user does not have permission to perform the requested action            |
| 404  | Not Found              | The call is not sent to the correct URL                                      |
| 405  | Method Not Allowed     | The HTTP verb is not correct for the intended call                           |
| 415  | Unsupported Media Type | The Content-Type header was not application/json                             |
| 422  | Unprocessable Entity   | The action can't be performed on the identifier provided                     |
