---
title: Line Item
name: Line Item
position: 4
visibility: file-specs
method: both
description: The details of an item within Item(Parent) & SKU(Child).
right_code: |

---

#### Line Item
_Supplier Fields_

uuid
: (string) Universal Unique Identifier for the Line Item

status
: (string) Status for the Line Item. Accepted Fields below
- "Unallocated"
- "Allocated"
- "Rejected"
- "HasTracking"
- "Backordered"
- "Cancelled"

item_uuid
: (string) Universal Unique Identifier for the item

item_name
: (string) Item Name

sku_uuid
: (string) Universal Unique Identifier for the SKU

sku_id
: (string) sku as provided by the Supplier

sku_name
: (string) sku Name

sku_title_variants
: (string) sku title variants

sku_special_instructions
: sku special instructions

cost
: (float) Cost of the sku

supplier_uuid
: (string) Universal Unique Identifier for the Supplier

supplier_name
: (string) Supplier name

tracking_numbers
: (object) The Tracking Numbers array parameter includes tracking number objects. Each include a tracking number, carrier, method, weight, cost, shipping date, and quantity.

allocation
: (object) The Allocation object contains quantity ordered, quantity allocated, quantity backordered, quantity rejected, and backorder date.

#### tracking_numbers (object)

tracking_number
: (string) Tracking number for this shipment

shipping_carrier
: (string) Shipping Carrier for this shipment

shipping_method
: (string) Shipping Method for this shipment

shipping_weight
: (string) Shipping Weight for this shipment

shipping_cost
: (string) Shipping Cost for this shipment

shipping_date
: (string) Date the order was shipped

quantity
: (integer) Number of items in the shipment

#### user (object)
_Retailer Fields_

name
: (string) Users full name

email
: (string) Users email address

#### allocation (object)
_Supplier Fields_

quantity_ordered
: (integer) The quantity ordered of the sku

quantity_allocated
: (integer) The Quantity Allocated by the Supplier for this Order

quantity_backordered
: (integer) Quantity Backordered is the quantity of the order that cannot be shipped because it is currently in a “backordered” state. If you allow the supplier to fulfill the order, this number is supposed to decrease to 0 as they get the item in-stock in their warehouse(s). When a Supplier gets a Backorder Date, they add it to the field labeled “backorder_date”.

quantity_rejected
:  (integer) Quantity Rejected by the Supplier is the Quantity that they simply cannot fulfill. Reasons may vary, such as state or federal law, customs, or being out-of-stock on an already discontinued product line.

backorder_date
: (string) Date that the Backordered SKU will be available for shipment. This date should be used as a tentative schedule which may help determine if waiting for the order is appropriate. Should this date be unacceptable, you may cancel the order with the “Cancel Order” API call.
