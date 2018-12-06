---
title: Tracking
name:
position: 2
visibility: file-specs
method:
description: The Tracking section
right_code: |

---

retailer_org_uuid
: (string) ***Required*** Retailers Organization Universal Unique Identifier for the organization

retailer_po
: (string) ***Required*** Retailer provided purchase order number

tracking_number
: (string) ***Required*** Order tracking number

sku_id
: (string) ***Required*** The SKU Identifier for the SKU as provided by the Supplier

quantity_shipped
: (integer) Quantity shipped

supplier_provided_sku_cost
: (decimal) Supplier provided SKU cost (2 decimal places)

supplier_po
: (string) Supplier provided purchase order number

supplier_provided_notes
: (string) Supplier provided notes

supplier_provided_order_attributes
: (array) Array of supplier provided Order Attribute objects

supplier_provided_line_item_attributes
: (array) Array of supplier provided Line Item objects

supplier_provided_drop_ship_fee
: (decimal) Supplier provided dropship fee (2 decimal places)

supplier_provided_order_fee
: (decimal) Supplier provided order fee (2 decimal places)

supplier_provided_tax
: (decimal) Supplier provided tax (2 decimal places)

supplier_provided_order_total
: (decimal) Supplier provided (2 decimal places)

supplier_provided_shipping_cost
: (decimal) Retailer provided shipping cost (2 decimal places)