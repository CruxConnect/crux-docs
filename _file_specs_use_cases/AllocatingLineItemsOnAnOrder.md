---
title: Allocating Line Items for Orders
name:
position: 4
visibility: file-specs
method:
description: How do I allocate line items on an order
right_code: |
  ~~~ bash
  retailer_po
  sku_id
  ---ONE-OF---
  quantity_accepted
  quantity_rejected
  quantity_backordered
  ------------
  backorder_date (to be used with quantity_backordered)
  ~~~
  {: title="Required Fields" }
  ~~~ bash
  ~~~
  {: title="Preferred Fields" }
  ~~~ bash
  supplier_po
  supplier_provided_notes
  supplier_provided_order_attributes
  supplier_provided_attribute_name
  supplier_provided_attribute_value
  supplier_provided_attribute_name
  supplier_provided_attribute_name
  supplier_provided_attribute_name
  supplier_provided_attribute_name
  supplier_provided_attribute_name
  supplier_provided_attribute_name

  ~~~
  {: title="Desired Fields" }

---
----
### File Sample
* <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/order_allocate_line_items_detail.xlsx">Allocate Order Line Items Download</a>

----
### File Details

----
### Best Practices

#### Suggested Uses