---
title: /orders/allocation/&ltorder_uuid&gt/
name: Allocate Order
position: 1.00
visibility: future
method: put
description: Allocate stock for a Retailer Order
right_code: |
  ~~~ json
    null
  ~~~
  {: title="Request" }


---
Allocate stock for a Retailer Order. Essentially accepting the entire order or a portion of the order by providing the order_uuid and providing the order_item_id and associated quantities per the allocation types.


### URL Parameters:

order_uuid
: (string) Universal Unique Identifier for the Order

### Request Parameters:

line_items
: (array) The Order Line Items array contains the individual Order Item objects

#### Order Item Object

line_item_uuid
: (string) The line item uuid for the product purchased by the Retailer

supplier_provided_po_number
: (string) Supplier provided purchase order number

supplier_provided_invoice_number
: (string) Supplier provided invoice number

allocation
: (object) The Allocation Object parameter includes the quantites accepted, rejected, and backordered.

#### Allocation Object

quantity_ordered
: (integer) The Quantity Ordered of the SKU

quantity_allocated
: (integer) The Quantity Allocated by the Supplier for this Order

quantity_backordered
: (integer) The Quantity Backordered is the quantity of the order that cannot be shipped because it is currently in a "backordered" state. If you allow the supplier to fulfill the order, this number is supposed to decrease to 0 as they get the item in-stock in their warehouse(s). When a Supplier gets a Backorder Date, they add it to the field labeled "backorder_date".

quantity_rejected
: (integer) The Quantity Rejected by the Supplier is the Quantity that they simply cannot fulfill. Reasons may vary, such as state or federal law, customs, or being out-of-stock on an already discontinued product line.

backorder_date
: (string) The Date that the Backordered SKU will be available for shipment. This date should be used as a tentative schedule which may help determine if waiting for the order is appropriate. Should this date be unacceptable, you may cancel the order with the "Cancel Order" API call.

### Response Parameters

line_items
: (array) Array of line item objects

#### Line Item Objects

line_item_uuid
: (string) The Universal Unique Identifier for the Item

quantity_shipped
: (integer) The Quantity of the Item included in the shipment associated with the Tracking Number

supplier_provided_sku_cost
: (decimal) The SKU cost (2 decimal places)

### Expected Response Codes

{% include links/response_codes.md %}
