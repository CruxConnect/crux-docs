---
title: /&ltorder_uuid&gt/invoices/
name: Get Order Invoices
position: 8.02
visibility: public
method: get
description: Get Order Invoice Details
right_code: |
  ~~~ json

  ~~~
  {: title="Request" }

  ~~~ json
  null
  ~~~
  {: title="Response" }

---
Get invoice details associated with a specific order

### URL Parameters:

order_uuid
: (string) Order Universal Unique Identifier


### Request Parameters:

invoice_uuid
: (string) The Universal Unique Identifier for the Invoice

address
: (object) Business address object

retailer_provided_notes
: (string) Retailer provided notes on the order

retailer_provided_order_attributes
: (array) Array of realtor provided order attribute objects

line_items
: (array) Array of line item objects

supplier_provided_drop_ship_fee
: (decimal) Supplier provided drop ship fee (2 decimal places)

supplier_provided_order_fee
: (decimal) Supplier provided order fee (2 decimal places)

supplier_provided_tax
: (decimal) Supplier provided tax (2 decimal places)

supplier_po_number
: (string) Supplier Purchase Order Number

supplier_provided_order_total
: (decimal) Supplier provided Order Total (2 decimal places)

#### Address Object

{% include timp/orders/address.md %}

#### Line Item Object

line_item_uuid
: (string) Line Item Universal Unique Identifier

sku_id
: (string) SKU ID

quantity_ordered
: (integer) Quantity Ordered

quantity_invoiced
: (integer) Quantity Invoiced

supplier_provided_sku_cost
: (decimal) Supplier provided SKU cost (2 decimal places)

supplier_provided_notes
: (decimal) Supplier provided notes (2 decimal places)

supplier_provided_order_attributes
: (array) Array of supplier provided order attribute objects

##### Retailer and Supplier Attribute Objects

{% include timp/orders/attributes.md %}

### Response Parameters:

invoice_uuid
: (string) The Universal Unique Identifier for the Invoice

### Expected Response Codes

{% include timp/links/response_codes.md %}
