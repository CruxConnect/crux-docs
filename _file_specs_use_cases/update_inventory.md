---
title: Update Inventory
name:
position: 2
visibility: file-specs
method:
description: How do I update inventory
right_code: |
  ~~~ bash
  item_id
  sku_id
  quantity_in_stock
  ~~~
  {: title="Required Fields" }
  ~~~ bash

  ~~~
  {: title="Preferred Fields" }
  ~~~ bash
  quantity_on_backorder
  backorder_date (required when using quantity_on_backorder)
  ~~~
  {: title="Desired Fields" }

---
----
### File Sample

* <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/inventory_update_detail.xlsx">Inventory Update Download</a>

----
### File Details

----
### Best Practices

#### Suggested Uses