---
title: Update Inventory
name:
position: 2
visibility: file-specs
method:
description: How do I update inventory?
right_code: |
  ~~~ bash
  item_id
  sku_id
  quantity_in_stock
  ~~~
  {: title="Required Fields" }
  ~~~ bash
  backorder_date (required when using quantity_on_backorder)
  ~~~
  {: title="Dependent Fields" }
  ~~~ bash
  quantity_on_backorder
  ~~~
  {: title="Desired Fields" }

---
----
### File Sample

* ***csv*** <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/csv/inventory_sample.csv">Inventory Sample Download</a>
* ***xlsx*** <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/xlsx/inventory_sample.xlsx">Inventory Sample Download</a>

----
### Submitting Files - FTP

#### File Details

##### Naming convention

inventory[anythingcangohere].csv
{: .info }
inventory[anythingcangohere].xlsx
{: .info }

- Character encoding (UTF-8)
- Line Feed (\n) required
- Proper naming conventions. (file names must not include spaces)

#### FTP Upload
1.	Create your file based on our sample files and specs, including all required fields.
2.	Log into your Crux-provided FTP
3.	Upload file inside ***/in*** directory

----
### Notes

  * Include all three required fields.