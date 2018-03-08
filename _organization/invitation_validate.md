---
title: /organizations/accept-invite/{token}/
name: Validate Invitation
method: get
visibility: internal
description: Validate a crux invitation token
---
### URL Parameters:

token
: (string) The invitation token

### Response Parameters:

email
: (string) The email address to which the invitation belongs

token
: (string) The invitation token

### Expected Response Codes:

| Code | Name      | Meaning                                      |
|------|----------------------------------------------------------|
| 200  | OK        | The token is valid                           |
| 201  | Created   | The token has expired. A new email was sent. |
| 404  | Not Found | The token is invalid                         |

{% include links/response_codes.md %}
