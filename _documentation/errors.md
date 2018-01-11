---
title: Errors
position: 3
---

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 201  | Created                | The API call was received and something was created                          |
| 204  | No Content             | The API call was received and we are performing the requested action         |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 405  | Method Not Allowed     | Generally, the HTTP verb is not correct for the intended call                |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |
| 422  | Unprocessable Entity   | Generally, the action can't be performed on the identifier provided          |
