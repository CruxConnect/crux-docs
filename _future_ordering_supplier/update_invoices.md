---
title: /&ltorder_uuid&gt/invoices/
name: Update Order Invoices
position: 9.03
visibility: public
method: post
description: Update Order Invoice Details
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
Update invoice details associated with a specific order

### URL Parameters:

order_uuid
: (string) Order Universal Unique Identifier


### Request Parameters:

invoice_number
: (string) ***Required*** Invoice Number

line_items
: (array) ***Required*** Array of Line Item objects


#### Line Item Object

line_item_uuid
: (string) ***Required*** Line Item Universal Unique Identifier

quanty_shipped
: (integer) Quantity shipped


### Response Parameters:

invoice_uuid
: (string) The Universal Unique Identifier for the Invoice

### Expected Response Codes

{% include timp/links/response_codes.md %}
