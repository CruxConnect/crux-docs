---
title: /orders/acknowledge/
name: Acknowledge Orders
position: 1.02
visibility: future-internal
method: put
description: Acknowledge Orders
right_code: |
  ~~~ json
  null
  ~~~
  {: title="Request" }

  ~~~ json
  null
  ~~~
  {: title="Response" }

---
Ackowledge Orders

### Response Parameters:

uuids
: (array) Array of Order UUID objects

#### Order UUID Object

order_uuid
: (string) Order Universal Unique Identifier

### Expected Response Codes

{% include timp/links/response_codes.md %}
