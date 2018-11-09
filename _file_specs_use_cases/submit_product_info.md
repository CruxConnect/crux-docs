---
title: Submitting Product Information
name:
position: 1
visibility: file-specs
method:
description: How do I submit product information to my catalog
right_code: |
  ~~~ bash
  item_id
  title
  sku_id
  pricing.[N].catalog
  pricing.[N].minimum_tier_quantity
  pricing.[N].cost
  ~~~
  {: title="Required Fields" }

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
  pricing.[N].shipping_cost
  pricing.[N].shipping_cost_is_estimate
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
  item_attribute.[N].name
  item_attribute.[N].value
  sku_distinguishing_attribute.[N].name
  sku_distinguishing_attribute.[N].value
  sku_nondistinguishing_attribute.[N].name
  sku_nondistinguishing_attribute.[N].value
  description
  ~~~
  {: title="Preferred Fields" }
  ~~~ bash
  ~~~
  {: title="Desired Fields" }

---
----
### File Sample

* <a href="https://s3-us-west-2.amazonaws.com/crux-kb/file-samples/supplier-use-cases/create_catalog_detail.xlsx">Create Catalog Download</a>

----
### File Details
  When there is an **[N]** in the field name it will be represented by a number to group related fields together
    - _e.g. Name, Value, and Type._

  Fields that use the **[N]** value are the:
  * 5 pricing options
  * 10 sku distinguishing attributes
  * 10 sku non distinguishing attributes

----
### Best Practices

The **create_catalog.csv** allows the user to create a catalog with items and skus.

  * The default unit of measurement metric values are **cm** & **g**
  * Always add a value in `pricing.[N].shipping_cost_is_estimate` otherwise the system will ignore the `pricing.[N].shipping_cost` field.

#### Suggested Uses

  * item_attribute
    - Used when it's a parent attribute. - _e.g. features, or fabric_
  * sku_distinguishing_attribute
    - Used when it's an absolute variant on the parent object. - _e.g. color or size_
  * sku_nondistinguishing_attribute
    - Used when it's at the sku level, but is a companion to an already distinguishing attribute. - _e.g. you've set color as a `sku_distinguishing_attribute`, then `color_code` can be set to `sku_distinguishing_attribute`_