---
title: Authentication
position: 2
right_code: |
  ~~~ javascript
  jQuery.ajax({
    url: "https://stable.projectthanos.com/api/organizations/transactions/",
    type: "GET",
    headers: {
        "Authorization": "Token YOUR_AUTHENTICATION_TOKEN",
    },
  })
  ~~~
  {: title="jQuery" }

  ~~~ bash
  curl "https://stable.projectthanos.com/api/organizations/transactions/" \
     -H 'Authorization: Token YOUR_AUTHENTICATION_TOKEN'
  ~~~
  {: title="Curl" }
---

You need to be authenticated for all API requests. In order to get authenticated, you must first send a "login" API call
with your username and password. The authentication token you receive is to be provided as a header in subsequent calls.

Add the auth_token as to calls as a header such as 'Authorization: Token \<auth_token\>'

You will experience errors if you do not include the authentication token. You may choose to also include your username
and password, although they are not required in subsequent calls.
