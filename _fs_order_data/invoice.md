---
title: Invoice
name:
position: 3
visibility: file-specs
method:
description:
right_code: |

---
retailer_org_uuid
: (string) ***Required*** Universal Unique Identifier for the Line Item.

retailer_po
: (string) ***Required*** The Purchase Order ID that you provide to identify your order.

invoice_number
: (string) ***Required*** Invoice number.

sku_id
: (string) ***Required*** Name of the product.

quantity_invoiced
: (integer) ***Required*** Quantity invoiced.

supplier_provided_sku_cost
: (decimal) ***Required*** Supplier provided SKU cost (2 decimal places)

supplier_provided_drop_ship_fee
: (float) Supplier provided dropship fee

supplier_provided_order_fee
: (float) Supplier provided order fee

supplier_provided_tax
: (float) Supplier provided tax

supplier_provided_order_total
: (float) Supplier provided order total

supplier_provided_shipping_cost
: (float) Supplier provided shipping cost

invoice_attributes
: (array) Array of Invoice Attribute objects

invoice_line_item_attributes
: (array) Array of Invoice Item Attribute objects

supplier_po
: (string) ***Required*** The Purchase Order ID that you provide to identify your order

supplier_provided_notes
: (string) Supplier provided notes

supplier_provided_order_attributes
: (array) Array of supplier provided Order Attribute objects

supplier_provided_line_item_attributes
: (array) Array of supplier provided Line Item objects
