---
title: /products/skus/search/completion/
name: Sku Completion
method: post
description: Give a partial sku id, get matching skus in return. Used for sku id autocompletion.
---
### Request Parameters:
partial
: (string) A partial sku id

### Response Parameters:

skus
: (array) An array of AutoCompletion SKUs

#### AutoCompletion SKU:

uuid
: (string) UUID of the sku

price_tiers
: (array) One or more Price Tiers

supplier_uuid
: (string) UUID for the supplier to which this SKU belongs

owner_uuid
: (string)

sku_id
: (string) The SKU ID that matches

item_title
: (string) The title of the Item

distinguishing_info
: (object) Distinguishing Info for this SKU

product_images
: (array) An array of Images for this SKU

is_discovery
: (bool) Is this SKU from the discovery catalog

#### Price Tier Object:

shipping_cost_is_estimate
: (bool) Is the shipping cost an estimate

minimum_tier_quantity
: (number) Minimum threshold to qualify for this tier of pricing

handling_cost
: (number) An additional charge from the supplier for handling this SKU

cost
: (number) The cost of the SKU at this price tier

shipping_cost_type
: (string) The type of shipping cost. One of: fixed, free, variable

cost_per_unit
: (number) The cost of each individual unit within a bundle

shipping_cost
: (number) The Shipping Cost per the SKU per the Price Tier

#### Distinguishing Info

condition
: (string) The condition of the sku. One of: new, used, refurbished

distinguishing_attributes
: (object) An object of key:value pairs. (e.g. `{ color: 'red', size: 9 }`)

number_of_units_bundled
: (number) The number of individual units bundled in this SKU

#### Image

uuid
: (string) The Universal Unique Identifier for the Item Product Image

url
: (string) The URL for the Item Product Image

width
: (number) The Image Width in pixels for the Item Product Image

height
: (number) The Image Height in pixels for the Item Product Image
