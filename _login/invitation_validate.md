---
title: /organizations/accept-invite/
name: Validate Invitation
method: get
visibility: internal
description: Validate a crux invitation token
---
### Request Parameters:

token
: (string) The invitation token

### Expected Response Codes:

| Code | Name                   | Meaning                             |
|------|--------------------------------------------------------------|
| 200  | OK                     | The token is valid                  |
| 404  | Not Found              | The token is invalid or has expired |

{% include links/response_codes.md %}
