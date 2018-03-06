---
title: /organizations/accept-invite/
name: Accept Invitation
method: post
visibility: internal
description: Create a CruxConnect account by accepting an invitation
---
### Request Parameters:

token
: (string) The invitation token

password
: (string) The invitation token

### Response Parameters:

| Code | Name                   | Meaning                             |
|------|--------------------------------------------------------------|
| 201  | Created                | Your account has been created       |
| 404  | Not Found              | The token is invalid or has expired |

{% include links/response_codes.md %}
