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

* ***csv*** <a href="/files/file-samples/csv/inventory_sample.csv">Inventory Sample Download</a>
* ***xlsx*** <a href="/files/file-samples/xlsx/inventory_sample.xlsx">Inventory Sample Download</a>

----
### Submitting Files - FTP

#### File Details

##### Naming convention

inventory_date.csv
{: .info }
inventory_date.xlsx
{: .info }

- Acceptable characters, [A-Za-z0-9-_]
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