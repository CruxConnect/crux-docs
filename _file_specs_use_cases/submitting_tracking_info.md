---
title: Submitting Tracking Info
name:
position: 5
visibility: file-specs
method:
description: How do I submit tracking information
right_code: |
  ~~~ bash
  retailer_po
  tracking_number
  sku_id
  ~~~
  {: title="Required Fields" }
  ~~~ bash
  quantity_shipped
  supplier_provided_sku_cost
  ~~~
  {: title="Preferred Fields" }
  ~~~ bash
  supplier_po
  supplier_provided_notes
  supplier_provided_order_attributes
  supplier_provided_attribute_name
  supplier_provided_attribute_value
  supplier_provided_drop_ship_fee
  supplier_provided_order_fee
  supplier_provided_tax
  supplier_provided_order_total
  supplier_provided_shipping_cost
  ~~~
  {: title="Desired Fields" }

---

----
### File Sample

* <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/add_tracking_detail.xlsx">Add Tracking Download</a>

----
### File Details

----
### Best Practices

#### Suggested Uses