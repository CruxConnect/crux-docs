---
title: Submitting Product Information
name:
position: 1
visibility: file-specs
method:
description: How do I submit product information?
right_code: |
  ~~~ bash
  item_id
  title
  sku_id
  pricing.1.catalog
  pricing.1.minimum_tier_quantity
  pricing.1.cost
  ~~~
  {: title="Required Fields" }

  ~~~ bash
  pricing.1.shipping_cost_is_estimate
  ~~~
  {: title="Dependent Fields" }

  ~~~ bash
  warranty
  return_policy
  manufacturer
  brand
  country_of_origin
  shipping_origin_country
  categories
  restrict_from_marketplaces
  other_marketplace_restriction
  fba_certified
  restrictions
  condition
  quantity_in_stock
  quantity_on_backorder
  backorder_date
  number_of_units_bundled
  pricing.1.shipping_cost
  pricing.1.shipping_cost_is_estimate
  minimum_advertised_price
  msrp
  sku_weight
  sku_weight_units
  sku_length
  sku_width
  sku_height
  sku_dimension_units
  package_weight
  package_weight_units
  package_length
  package_width
  package_height
  package_dimension_units
  upca
  ean13
  gtin14
  isbn
  asin
  mpn
  product_images_for_item
  product_images_for_sku
  item_attribute.1.name
  item_attribute.1.value
  sku_distinguishing_attribute.1.name
  sku_distinguishing_attribute.1.value
  sku_nondistinguishing_attribute.1.name
  sku_nondistinguishing_attribute.1.value
  description
  ~~~
  {: title="Preferred Fields" }

---
----
### File Sample

* ***csv*** <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/csv/product_sample.csv">Product Sample Download</a>
* ***xlsx*** <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/xlsx/product_sample.xlsx">Product Sample Download</a>

----
### Submitting Files - FTP

#### File Details

##### Naming convention

product[anythingcangohere].csv
{: .info }
product[anythingcangohere].xlsx
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

  * The default unit of measurement metric values are **cm** & **g**
  * item_attribute
    - Used when it's a parent attribute. - _e.g. features, or fabric_
  * sku_distinguishing_attribute
    - Used when it's an absolute variant on the parent object. - _e.g. color or size_
  * sku_nondistinguishing_attribute
    - Used when it's at the sku level, but is a companion to an already distinguishing attribute. - _e.g. you've set color as a `sku_distinguishing_attribute`, then `color_code` can be set to `sku_distinguishing_attribute`_