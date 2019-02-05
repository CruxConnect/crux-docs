---
title: Adding Order/Line Item Attributes
name:
position: 8
visibility: file-specs
method:
description: How do I add order/line item attributes?
right_code: |
  ~~~ bash
  retailer_org_uuid
  retailer_po
  supplier_provided_notes
  supplier_provided_order_attributes
  sku_id
  supplier_provided_order_line_item_attributes
  ~~~
  {: title="Desired Fields" }

---

----
### File Sample

* ***csv*** <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/csv/attributes_sample.csv">Attributes Sample Download</a>
* ***xlsx*** <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/xlsx/attributes_sample.xlsx">Attributes Sample Download</a>

----
### Submitting Files - FTP

#### File Details

##### Naming convention

attributes[anythingcangohere].csv
{: .info }
attributes[anythingcangohere].xlsx
{: .info }

- Character encoding (UTF-8)
- Line Feed (\n) required
- Proper naming conventions. (file names must not include spaces)

#### FTP Upload
1.	Create your file based on our sample files and specs, including all required fields.
2.	Log into your Crux-provided FTP
3.	Upload file inside ***/in*** directory