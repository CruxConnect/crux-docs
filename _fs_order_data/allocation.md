---
title: Allocation
name:
position: 1
visibility: file-specs
method:
description:
right_code: |

---

retailer_org_uuid
: (string) Universal Unique Identifier for the Line Item

retailer_po
: (string) Required The Purchase Order ID that you provide to identify your order

sku_id
: (string) ***Required*** Name of the product.

quantity_accepted
: (object) Required The Quantity Accepted by the supplier

quantity_rejected
: (integer) Required Quantity Rejected by the Supplier is the Quantity that they cannot fulfill.

quantity_backordered
: (integer) Current order of a product that is out of stock

backorder_date
: (string) Date that the Backordered SKU will be available for shipment. This date should be used as a tentative schedule which may help determine if waiting for the order is appropriate. Should this date be unacceptable, you may cancel the order with the “Cancel Order” API call.

supplier_po
: (string) Required The Purchase Order ID that you provide to identify your order

supplier_provided_notes
: (string) Supplier provided notes

supplier_provided_order_attributes
: (array) Array of supplier provided Order Attribute objects

supplier_provided_line_item_attributes
: (array) Array of supplier provided Line Item objects
