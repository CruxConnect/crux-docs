---
title: Product Import/Export CSV File Format
visibility: hidden
position: 5
---
The product specification file allows items (the item is the parent) and skus (the sku is the child with variant attributes) to be imported and exported.  Each item may be associated with multiple skus and item level information should be duplicated across its skus.

Fields do not have to be in a particular order.

[N] => an integer

### Item Level Info

item_id
: (string(max 256))  [**REQUIRED**] The Item Identifier is the identifier for the item as provided by the supplier.

supplier_uuid
: (string) [**RETAILER-ONLY**, **EXPORT-ONLY**] Universal Unique Identifier for the Supplier

title
: (string(max 256)) [**REQUIRED**] Item Title

description
: (string(max 65,535)) Item Description

warranty
: (string(max 65,535)) Item Warranty

return_policy
: (string(max 65,535)) Item Return Policy

manufacturer
: (string(max 128)) Item Manufacturer

brand
: (string(max 128)) Item Brand

country_of_origin
: (string(2)) Valid 2 letter country code for the country of origin (e.g. 'CA')

shipping_origin_country
: (string(2)) Valid 2 letter country code for the shipping origin country (e.g. 'US')

categories
: (string) The categories to which the item belongs.
: When building the paths, '>' is within the path delimiter and '\|' is between the path delimiter.
: Example: 'Home > Decor > Bidets \| Outdoor > Sports > Bats'

restrict_from_marketplaces
: (string) Marketplace Restrictions.  Restrictions are comma_separated.  Example: 'amazon, ebay, newegg, overstock, walmart'

other_marketplace_restriction
: (string(max 256)) Other Marketplace Restrictions

fba_certified
: (bool) The Fulfillment By Amazon (FBA) Certified parameter indicates whether this supplier has FBA set up on this Item.

custom_attribute.[N].name
: (string(max 128)) Custom Attribute Name

custom_attribute.[N].value
: (string(max 256)) Custom Attribute Value

custom_attribute.[N].type
: (string) Custom Attribute Type.  Can be one of: 'str', 'int', 'float', 'bool'

product_images_for_item
: (string) Uri(s) for the product image.  Individual URIs are comma separated uris. Duplicate uris across sku or item will reference the same product image

### SKU Level Info

sku_id
: (string(max 256)) [**REQUIRED**] The SKU Identifier for the SKU as provided by the Supplier

restrictions
: (string) Restrictions imposed on the SKU.  Can be one of: 'tmpunavail', 'discontd'

condition
: (string) The condition of the SKU.  Can be one of: 'new', 'used', 'refurb'

quantity_in_stock
: (integer) Value must be >= 0.  Quantity of SKU in stock

quantity_on_backorder
: (integer) Value must be >= 0. Quantity of SKU on backorder

number_of_units_bundled
: (integer) Value must be >= 0. Number of units bundled within the SKU

minimum_advertised_price
: (float) Minimum Advertised Price

msrp
: (float) Manufacturer Suggested Retail Price

product_images_for_sku
: (string) URIs for the product image.  Individual URIs are comma separated uris. Duplicate uris across sku or item will reference the same product image

inventory_lists
: (string) [**RETAILER-ONLY**, **EXPORT-ONLY**] Comma seperated Inventory List UUIDs.  Example: '03e697-6a17-4dd1-939b-3d7ca9676b1c, 266a9a41-58a0-429e-8275-791f169789d1'


#### Measurements

weight_units
: (string) The units utilized by the supplier for weight (‘g’, ‘kg’, ‘lb’, and ‘oz’ are potential options, where ‘g’ is the default)

dimension_units
: (string) The units utilized by the supplier for dimensions ('cm', 'm', 'in', and 'ft' are potential options, where 'cm' is the default)

weight
: (float) Weight in weight_units - default in grams (g)

length
: (float) Length in dimension_units - default in centimeters (cm)

width
: (float) Width in dimension_units - default in centimeters (cm)

height
: (float) Height in dimension_units - default in centimeters (cm)

#### Package Measurements

package_weight_units
: (string) The units utilized by the supplier for weight (‘g’, ‘kg’, ‘lb’, and ‘oz’ are potential options, where ‘g’ is the default)

package_dimension_units
: (string) The units utilized by the supplier for dimensions ('cm', 'm', 'in', and 'ft' are potential options, where 'cm' is the default)

package_weight
: (float) Package Weight in package_weight_units - default in grams (g)

package_length
: (float) Package Length in package_dimension_units - default in centimeters (cm)

package_width
: (float) Package Width in package_dimension_units - default in centimeters (cm)

package_height
: (float) Package Height in package_dimension_units - default in centimeters (cm)

#### Identifiers

upca
: (string(12)) UPCA Product Identifier

ean13
: (string(13)) EAN13 Product Identifier

gtin14
: (string(14)) GTIN14 Product Identifier

isbn
: (string(13)) ISBN Product Identifier

asin
: (string(10)) ASIN Product Identifier

mpn
: (string(128)) Product Identifier

#### SKU Distinguishing Attributes

sku_distinguishing_attribute.[N].name
: (string(max 128)) Distinguishing Attribute Name

sku_distinguishing_attribute.[N].value
: (string(max 256)) Distinguishing Attribute Value

sku_distinguishing_attribute.[N].type
: (string) Distinguishing Attribute Type.  Can be one of 'str', 'int', 'float', 'bool'

#### SKU Non Distinguishing Attributes

sku_nondistinguishing_attribute.[N].name
: (string(max 128)) Non-Distinguishing Attribute Name

sku_nondistinguishing_attribute.[N].value
: (string(max 256)) Non-Distinguishing Attribute Value

sku_nondistinguishing_attribute.[N].type
: (string) Non-Distinguishing Attribute Type.  Can be one of 'str', 'int', 'float', 'bool'

#### Pricing

pricing.[N].catalog
: (string) [**SUPPLIER-ONLY**  REQUIRED] Catalog Name

pricing.[N].minimum_tier_quantity
: (int) [REQUIRED] Minimum Tier Quantity

pricing.[N].cost
: (float) [REQUIRED] Cost

pricing.[N].shipping_cost
: (float) Shipping Cost

pricing.[N].shipping_cost_is_estimate
: (bool) Is Shipping Cost an estimate

pricing.[N].handling_cost
: (float) Handling Cost

