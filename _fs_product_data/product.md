---
title: Product
name:
position: 1
visibility: file-specs
method:
description: The Product file covers both the item(Parent) & sku(Child) catalog information.
right_code: |

---

item_id
: (string) ***Required*** Unique identifier for the parent product.

sku_id
: (string) ***Required*** Name of the product.

title
: (string) ***Required*** Summary of the product information and/or specifications. Valid HTML is allowed, ensure that all tags are closed.

warranty
: (string) Product specific warranty.

return_policy
: (string) Rules to establish a process in which customers can return or exchange unwanted or defective items.

manufacturer
: (string) Manufacturer of the product.

brand
: (string) Brand name of the product.

country_of_origin
: (string, ISO Alpha-2) The country where the product was manufactured. Must be a <a href="https://www.nationsonline.org/oneworld/country_code_list.htm" target="_blank">2-digit ISO country code</a>.

shipping_origin_country
: (string, ISO Alpha-2) The country where the product is shipping from. Must be a <a href="https://www.nationsonline.org/oneworld/country_code_list.htm" target="_blank">2-digit ISO country code</a>.

categories
: (array) The division in which items are organized based on shared characteristics.

`>` = Category Path Separator
{: .info }
`|` = Category Separator
{: .info }

restrict_from_marketplaces
: (string) Marketplaces in which the item can not be listed.
##### ***Values***:
- amazon
- ebay
- newegg
- overstock
- walmart

other_marketplace_restrictions
: (string) Marketplaces that items cannot be listed and don't fit in the accepted values of `restrict_from_marketplaces` field.

fba_certified
: (boolean) Fulfillment by Amazon ceritifed.

restrictions
: (string) Current status of the product if it is not in stock. Accepted Values below

condition
: (string) The state in which the item is being sold in.

quantity_in_stock
: (integer) Quantity currently available to be shipped

quantity_on_backorder
: (integer) Current order of a product that is out of stock

backorder_date
: (string) Date that the Backordered SKU will be available for shipment. This date should be used as a tentative schedule which may help determine if waiting for the order is appropriate. Should this date be unacceptable, you may cancel the order with the “Cancel Order” API call.

number_of_units_bundled
: (integer) The combined amount of units in the product bundle

pricing.1.catalog
: (string, alphanumeric, underscores) ***Required*** Used to organize the product into a particular catalog.

pricing.1.minimum_tier_quantity
: (integer) ***Required***

pricing.1.cost
: (float) ***Required*** Cost of the product.

pricing.1.shipping_cost
: (float) Cost to ship the packaged product.

pricing.1.shipping_cost_is_estimate
: (boolean) `true` or `false` value to indict if the cost is actual or estimated.

minimum_advertised_price
: (float) The lowest price a retailer can advertise the product for sale

msrp
: (float) Manufacturer's Suggested Retail Price is the price at which the manufacturer recommends that the retailer sell the product.

sku_weight
: (float) The product weight.

sku_weight_units
: (string) The unit of measurement used to provide a weight value to the `sku_weight` field.

sku_length
: (float) The length of the product.

sku_width
: (float) The width of the product.

sku_height
: (float) The height of the product.

sku_dimension_units
: (string) The unit of measurement used to provide the length, width, and height of the product.
##### ***Values***:
- _Default:_ cm
- m
- in
- ft

package_weight
: (float) The weight of the product when packaged for shipping.

package_weight_units
: (string) The unit of measurement used to provide a weight value to the `package_weight` field.

package_length
: (float) The length of the product when packaged for shipping.

package_width
: (float) The width of the product when packaged for shipping.

package_height
: (float) The height of the product when packaged for shipping.

package_dimension_units
: (string) The unit of measurement used to provide the length, width, and height of the product.

upca
: (string) UPC-A consists of 12 numeric digits, that are uniquely assigned to each trade item.

ean13
: (string) The European Article Number (EAN) is a barcode standard, a 12- or 13-digit product identification code. Each EAN uniquely identifies the product, manufacturer, and its attributes; typically, the EAN is printed on a product label or packaging as a bar code.

gtin14
: (string) The GTIN is a globally unique 14-digit number used to identify trade items, products, or services.

isbn
: (string) The International Standard Book Number (ISBN) is a unique numeric commercial book identifier. An ISBN is assigned to each edition and variation (except reprintings) of a book.

asin
: (string) Amazon Standard Identification Number. It’s a 10-charcter alphanumeric unique identifier that’s assigned by Amazon.com and its partners. It’s used for product-identification within Amazon.com organization. ASINs are only guaranteed unique within a marketplace.

mpn
: (string) A manufacturer part number is a series of numbers and/or letters that has been given to a part by the manufacturer. An MPN identifies the part as belonging to and originating from that one manufacturer. Each part the manufacturer makes has a different MPN.

product_images_for_item
: (string) Image provide to offer a visual of the product. Duplicate URLs across a sku or item will reference the same Product Image.


product_images_for_sku
: (string) Image provide to offer a visual of the product. Duplicate URLs across a sku or item will reference the same Product Image.

description
: (string) Summary of the product information and/or specifications. Valid HTML is allowed, ensure that all tags are closed.

----
item_attribute.1.name
: (string) Name used for a parent attribute. - e.g. features, or fabric

item_attribute.1.value
: (string) Value used for a parent attribute. - e.g. wireless, or linen

20 `item_attribute` fields must be present.
{: .info }

sku_distinguishing_attribute.1.name
: (string) Name used when it’s an absolute variant on the parent object. - e.g. color or size

sku_distinguishing_attribute.1.value
: (string) Value used when it’s an absolute variant on the parent object. - e.g. green or medium

5 `sku_distinguishing_attribute` fields must be present.
{: .info }

sku_nondistinguishing_attribute.1.name
: (string) Name used when it’s at the sku level, but is a companion to an already distinguishing attribute. - e.g. you’ve set color as a `sku_distinguishing_attribute`, then `color_code` can be set to `sku_distinguishing_attribute`

sku_nondistinguishing_attribute.1.value
: (string) Value used when it’s at the sku level, but is a companion to an already distinguishing attribute. - e.g. you’ve set color as a `sku_distinguishing_attribute`, then `color_code` can be set to `sku_distinguishing_attribute`

10 `sku_nondistinguishing_attribute` fields must be present.
{: .info }
