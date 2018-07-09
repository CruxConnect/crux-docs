---
title: /orders/tracking/&ltorder_uuid&gt/&lttracking_number&gt/
name: Update Order With New Tracking Number - Supplier
position: 1.01
visibility: public
method: put
description: Update an exsiting tracking number
right_code: |
  ~~~ json
  null
  ~~~
  {: title="Request" }

  ~~~ json
  null
  ~~~
  {: title="Response" }

---
Update the information associated with an existing tracking number.

### URL Parameters

<!-- task: update url to programmatically generate tracking number -->

order_uuid
: (string) The Universal Unique Identifier for the Order

tracking_number
: (string) The tracking number to be updated

### Request Parameters:

new_tracking_number
: (string) New tracking number

package_ship_cost
: (decimal) Package shipping cost (2 decmial places)

supplier_provided_carrier
: (string) Supplier provided carrier (e.g. UPS)

supplier_provided_method
: (string) Supplier provided shipping method (e.g. Ground)

package_weight
: (string) Package weight

package_ship_date
: (string) package ship date

line_items
: (array) An array of line item objects

#### Line Item Objects

quantity_shipped
: (integer) Quantity shipped

line_item_uuid
: (string) Line Item Universal Unique Identifier

supplier_provided_sku_cost
: (decimal) Supplier provided SKU cost (2 decimal places)

### Expected Response Codes

{% include links/response_codes.md %}
