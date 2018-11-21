---
title: Invoice
name:
position: 3
visibility: file-specs
method:
description: The Invoice
right_code: |

---
retailer_org_uuid
: (string) Universal Unique Identifier for the Line Item.

retailer_po
: (string) Required The Purchase Order ID that you provide to identify your order.

invoice_number
: (string) Required Invoice number.

sku_id
: (string) Name of the product.

quantity_invoiced
: (integer) Quantity invoiced.

supplier_provided_sku_cost
: (decimal) Supplier provided SKU cost (2 decimal places)

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