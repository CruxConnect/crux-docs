---
title: Update Order Fees
name:
position: 7
visibility: file-specs
method:
description: How do I update order fees?
right_code: |
  ~~~ bash
  supplier_po
  ~~~
  {: title="Required Fields" }

  ~~~ bash
  supplier_provided_dropship_fee
  supplier_provided_order_fee
  supplier_provided_tax
  supplier_provided_order_total
  ~~~
  {: title="Preferred Fields" }

---

----
### File Sample

* ***csv*** <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/csv/fees_sample.csv">Fees Sample Download</a>
* ***xlsx*** <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/xlsx/fees_sample.xlsx">Fees Sample Download</a>

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