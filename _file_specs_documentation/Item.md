---
title: Item
name:
position: 1
visibility: file-specs
method:
description: The Item section covers all item related parameters. The item parameters relate to the Parent Product.
right_code: |

---
#### Item
_Supplier Fields_

catalog_name
: (string) Unique identifier for the catalog of parent(item_id) and child(sku_id) products.

item_id
: (string) Unique identifier for the parent product.

title
: (string) Name of the product.

description
: (string) Summary of the product information and/or specifications. Valid HTML is allowed, ensure that all tags are closed.

warranty
: (string) Product specific warranty.

return_policy
: (string) Rules to establish a process in which customers can return or exchange unwanted or defective items.

manufacturer
: (string) Manufacturer of the product.

brand
: (string) Brand name of the product.

country_of_origin
: (string) The country where the product was manufactured. Must be a 2-digit ISO country code.

shipping_origin_country
: (string) ISO country code where the product is shipping from.

categories
: (array) The division in which items are organized based on shared characteristics.

restrict_from_marketplaces
: (string) Accepted Values below
- amazon
- ebay
- newegg
- overstock
- walmart

other_marketplace_restrictions
: (string) Marketplaces that items cannot be listed and don't fit in the accepted values of `restrict_from_marketplaces` field.

fba_certified
: (boolean) Fulfillment by Amazon ceritifed.

#### Supplier (object)
_Supplier Fields_

supplier_uuid
: (string) Universal Unique identifier for the Supplier

supplier_name
: (string) Supplier name

#### product_images (object)
_Supplier Fields_

uuid
: (string) Universal Unique identifier for the sku product image

uri
: (string) URI (Uniform Resource Identifier) for the sku product image

uri_type
: (string) Uri Type can be one of 'url' or 'filename'

width
: (integer) The image width in pixels for the sku product image

height
: (integer) The image height in pixels for the sku product image

#### product_videos (object)
_Supplier Fields_

uuid
: (string) The Universal Unique Identifier for the sku product video

uri
: (string) Uniform Resource Identifier for the sku product video

uri_type
: (string) Uri Type can be one of 'url' or 'filename'

