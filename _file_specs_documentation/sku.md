---
title: SKU
name: SKU
position: 2
visibility: file-specs
method: both
description: The sku section covers all sku related parameters. The sku parameters relate to the Child Product.
right_code: |

---

#### SKU
_Supplier Fields_

sku_id
: (string) Unique identifier for the child product

restrictions
: (string) Current status of the product if it is ***not*** in stock.
Accepted Values below
- tmpunavail (Temporarily Unavailable)
- discontd (Discontinued)

condition
: (string) The state in which the item is being sold in.

quantity_in_stock
: (integer ) Quantity currently available to be shipped

quantity_on_backorder
: (integer) Current order of a product that is out of stock

number_of_units_bundled
: (integer) The combined amount of units in the product bundle

minimum_advertised_price
: (float) The lowest price a retailer can advertise the product for sale

msrp
: (float) Manufacturer's Suggested Retail Price is the price that the manufacturer recommends the retailer sell the product at

uuid
: (string) Universal Unique Identifier for the sku

#### item (object)
_Supplier Fields_

item_uuid
: (string) Universal Unique Identifier for the item

#### price_tier (object)
_Supplier Fields_

handling_cost
: (float) Handling cost for the item at the price tier

shipping_cost_type
: (string/enum) Shipping cost type.
Accepted Values below.
- "Fixed"
- "Free"
- "Variable"

shipping_cost_estimate
: (boolean) Value showing if the shipping cost is actual or estimate.

cost
: (float) Cost of the product

cost_per_unit
: (float) Unit cost of the product

shipping_cost
: (float) Cost to ship the packaged product

minimum_tier_quantity
: (integer) Minimum quantity purchased to qualify for the price tier

#### catalog (object)
_Supplier Fields_

name
: (string) Supplier Name

uuid
: (string) Universal Unique Identifier for the Supplier

#### product_images (object)
_Supplier Fields_

uuid
: Universal Unique Identifier for the sku product image

uri
: (string) URI (Uniform Resource Identifier) for the sku product image

uri_type
: (string/enum) Uri Type can be one of 'url' or 'filename'

width
: (integer) Image width in pixels for the sku product image

height
: (integer) Image height in pixels for the sku product image

#### product_videos (object)
_Supplier Fields_

uuid
: Universal Unique Identifier for the sku product video

uri
: (string) URI (Uniform Resource Identifier) for the sku product video

uri_type
: (string/enum) Uri Type can be one of 'url' or 'filename'

#### measurements (object)
_Supplier Fields_

weight_units
: (string/enum) The unit of measurement used to provide a weight value to the `sku_weight` field.
Accepted values below.
- "g" (default)
- "kg"
- "lb"
- "oz"

weight
: sku weight in relation to the `weight_unit` field

dimension_units
: (string/enum) The unit of measurement used to provide the length, width, and height of the product.
Accepted values below.
- "cm" (default)
- "m"
- "in"
- "ft"

length
: (float) The length of the sku in relation to the `dimension_units` field

width
: (float) The width of the sku in relation to the `dimension_units` field

height
: (float) The height of the sku in relation to the `dimension_units` field

#### package measurements (object)
_Supplier Fields_

weight_units
: (string/enum) The unit of measurement used to provide a weight value to the `weight` field.
Accepted values below.
- "g" (default)
- "kg"
- "lb"
- "oz"

weight
: The weight of the sku when packaged for shipping in relation to the `weight_units` field.

dimension_units
: (string/enum) The unit of measurement used to provide the length, width, and height of the packaged sku.
Accepted values below.
- "cm" (default)
- "m"
- "in"
- "ft"

length
: (float) The length of the product when packaged for shipping in relation to the `dimension_units` field.

width
: (float) The width of the product when packaged for shipping in relation to the `dimension_units` field.

height
: (float) The height of the product when packaged for shipping in relation to the `dimension_units` field.

#### product_identifiers (object)
_Supplier Fields_

upca
: (string) UPC-A consists of 12 numeric digits, that are uniquely assigned to each trade item.

ean13
: (string) The European Article Number (EAN) is a barcode standard, a 12- or 13-digit product identification code. Each EAN uniquely identifies the product, manufacturer, and its attributes; typically, the EAN is printed on a product label or packaging as a bar code.

gtin14
: (string) The GTIN is a globally unique 14-digit number used to identify trade items, products, or services.

isbn
: (string) The International Standard Book Number (ISBN) is a unique numeric commercial book identifier. An ISBN is assigned to each edition and variation (except reprintings) of a book.

asin
: (string) Amazon Standard Identification Number. It's a 10-charcter alphanumeric unique identifier that's assigned by Amazon.com and its partners. It's used for product-identification within Amazon.com organization. ASINs are only guaranteed unique within a marketplace.

mpn
: (string) A manufacturer part number is a series of numbers and/or letters that has been given to a part by the manufacturer. An MPN identifies the part as belonging to and originating from that one manufacturer. Each part the manufacturer makes has a different MPN.

#### inventory_lists (object)
_Retailer Fields_

uuid
: (string) Universal unique identifier for the Inventory List

name
: (string) The naming associated to the Inventory List

#### supplier (object)
_Supplier Fields_

uuid
: (string) Universal Unique Identifier for the Supplier

name
: (string) Supplier Name