---
title: Submitting an Invoice
name:
position: 6
visibility: file-specs
method:
description: How do I submit an Invoice?
right_code: |
  ~~~ bash
  retailer_org_uuid
  retailer_po
  invoice_number
  sku_id
  quantity_invoiced
  supplier_provided_sku_cost
  ~~~
  {: title="Required Fields" }

  ~~~ bash
  supplier_provided_drop_ship_fee
  supplier_provided_order_fee
  supplier_provided_tax
  supplier_provided_order_total
  supplier_provided_shipping_cost
  ~~~
  {: title="Preferred Fields" }

---

----
### File Sample

* ***csv*** <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/csv/invoice_sample.csv">Invoice Sample Download</a>
* ***xlsx*** <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/xlsx/invoice_sample.xlsx">Invoice Sample Download</a>

----
### Submitting Files - FTP

#### File Details

##### Naming convention

invoice_date.csv
{: .info }
invoice_date.xlsx
{: .info }

- Acceptable characters, [A-Za-z0-9-_]
- Character encoding (UTF-8)
- Line Feed (\n) required
- Proper naming conventions. (file names must not include spaces)

#### FTP Upload
1.	Create your file based on our sample files and specs, including all required fields.
2.	Log into your Crux-provided FTP
3.	Upload file inside ***/in*** directory

