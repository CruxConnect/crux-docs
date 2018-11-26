---
title: Allocating Line Items for Orders
name:
position: 4
visibility: file-specs
method:
description: How do I allocate line items on an order?
right_code: |
  ~~~ bash
  retailer_po
  sku_id
  ---ONE-OF---
  quantity_accepted
  quantity_rejected
  quantity_backordered
  ------------
  ~~~
  {: title="Required Fields" }

  ~~~ bash
  backorder_date (to be used with quantity_backordered)
  ~~~
  {: title="Dependent Fields" }

  ~~~ bash
supplier_po
supplier_provided_notes
supplier_provided_order_attributes
supplier_provided_drop_ship_fee
supplier_provided_order_fee
supplier_provided_tax
supplier_provided_order_total
supplier_provided_sku_cost
supplier_provided_shipping_cost
  ~~~
  {: title="Desired Fields" }

---
----
### File Sample

* ***csv*** <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/csv/allocation_sample.csv">Allocation Sample Download</a>
* ***xlsx*** <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/xlsx/allocation_sample.xlsx">Allocation Sample Download</a>

----
### Submitting Files - FTP

#### File Details

##### Naming convention

filetype_date.csv
{: .info }
filetype_date.xlsx
{: .info }

- Character encoding (UTF-8)
- Line Feed (\n) preferred
- Proper naming conventions. (file names must not include spaces)

#### FTP Upload
1.	Create your file based on our sample files and specs, including all required fields.
2.	Log into your Crux-provided FTP
3.	Upload file inside ***/in*** directory

----
### Submitting Allocation - Crux Website

1.	On the Dashboard, go to ***Orders Awaiting Allocation***, click the order you wish to allocate
  - or go to the ***Allocate*** tab to view orders pending allocation.
2.	Enter the amount you are accepting under ***Amount Accepting***
3.	If one or more items are on backorder, enter the amount under ***Amount Backordered***; if there are no backordered items, enter 0. If available, provide the date that the backordered items will be available under ***Backordered Until***.
•	To export one or more orders into a spreadsheet, select the checkbox next to the order and click on the red ***Export*** button at the top.