---
title: Line Item
name:
position: 6
visibility: file-specs
method:
description: Line Item II
right_code: |
  ~~~ bash
  South Sudan tribespeople, circa 1905
  ~~~
  {: title="Manufacturer Example" }
---

#### Line Item
_Supplier Fields_

line_item_uuid
: (string) ***Required*** The line Item UUID for the product purchased by the Retailer

allocation
: (object) ***Required*** The Allocation Object parameter includes the quantites accepted, rejected, and backordered.

quantity_accepted
: (object) ***Required*** The Quantity Accepted by the supplier

quantity_rejected
: (integer) ***Required*** Quantity Rejected by the Supplier is the Quantity that they cannot fulfill.

quantity_backordered
: (integer) Quantity Backordered is the quantity of the order that cannot be shipped because it is currently in a “backordered” state.

backorder_date
: (string) Date that the Backordered SKU will be available for shipment.

line_item_status
: (string) Line item status

line_item_designation
: (string) Line item designation

quantity_shipped
: (integer) ***Required*** Quantity shipped

supplier_provided_sku_cost
: (float) Supplier provided SKU cost

package_uuid
: (string) Package Universal Unique Identifier

supplier_provided_order_attributes
: (object) An array of supplier provided order attribute objects

quantity_invoiced
: (integer) Quantity invoiced

supplier_proivided_sku_cost
: (float) Supplier provided sku cost

#### supplier_provided_order_attributes
_Supplier Fields_

attribute_name
: (string) Attribute name

attribute_value
: (string) Attribute value