---
title: /orders/attributes/&ltorder_uuid&gt/
name: Update Order Attributes
position: 1.01
visibility: public
method: post
description: Update Order Attributes
right_code: |
  ~~~ json

  ~~~
  {: title="Request" }

  ~~~ json
  null
  ~~~
  {: title="Response" }

---
Update Order Attributes

### URL Parameters:

order_uuid
: (string) The Universal Unique Identifier for the Order

### Request Parameters:

retailer_provided_notes
: (string) Retailer provided notes

retailer_provided_order_attributes
: (array) Array of retail provided Order Attribute objects

line_items
: (array) Array of line item objects

#### Line Item Objects

line_item_uuid
: (string) Line item Universal Unique Identifier

supplier_provided_notes
: (string) Supplier provided notes

supplier_provided_order_attributes
: (array) Array of supplier provided order attribute objects

#### Retailer and Supplier Order Attribute Object

{% include timp/orders/attributes.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}

