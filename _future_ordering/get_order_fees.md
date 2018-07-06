---
title: /orders/fees/&ltorder_uuid&gt/
name: Set Order Fees
position: 1.00
visibility: public
method: put
description: Set the Fees for an existing order.
right_code: |
  ~~~ json
    null
  ~~~
  {: title="Request" }

---
Allows supplier and retailer to specify their respective order fees. There are no additional CruxConnection fees.

### URL Parameters

order_uuid
: (string) Order Univeral Unique Identifier

### Request Parameters:

supplier_provided_drop_ship_fee
: (decimal) Supplier provided drop ship fee (2 decimal positions)

supplier_provided_order_fee
: (decimal) Supplier provided order fee (2 decimal places)

supplier_provided_tax
: (decimal) Supplier provided tax (2 decimal places)

supplier_po_number
: (string) Supplier provided purchase order number

supplier_provided_order_total
: (decimal) Supplier provided (2 decimal places)

line_items
: (array) Array of line item objects

retailer_provided_tax
: (decimal) Retail provided tax (2 decimal places)

retailer_provided_order_fee
: (decimal) Retailer provided fee (2 decimal places)

retailer_provided_shipping_cost
: (decimal) Retailer provided shipping cost (2 decimal places)

retailer_provided_drop_ship_fee
: (decimal) Retail provided drop ship fee (2 decimal places)

#### Line Item Object

line_item_uuid
: (string) Line item universal unique identifier

supplier_provided_sku_cost
: decimal Supplier provide sku cost(2 decimal places)

### Expected Response Codes

{% include links/response_codes.md %}
