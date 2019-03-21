---
title: Orders
name:
position: 4
visibility: file-specs
method:
description:
right_code: |

---

retailer_po
: (string) ***Required*** The Purchase Order ID that you provide to identify your order

order_uuid
: (string) Universal Unique Identifier for the Order

supplier_org_uuid
: (string) Universal Unique Identifier for the Supplier

requested_shipping_carrier
: (string) Shipping carrier requested upon order.

requested_shipping_method
: (string) Shipping method requested upon order.

sku_id
: (string) ***Required*** Name of the product.

sku_title_variants
: (string) Alternate title for sku

retailer_provided_sku_cost
: (string) Cost provided by Retailer

line_item_uuid
: (string) Universal Unique Identifier for the Line Item

line_item_special_instructions
: (string) Retailer provided instructions

quantity
: (string) Quantity ordered

business_name
: (string) Retailer provided business name

name
: (string) Name provided on order

phone
: (string) Phone provided on order

address1
: (string) Additional address field

address2
: (string) Additional address field

city
: (string) City provided on order
state
: (string) State provided on order

country
: (string) Country provided on order

postal_code
: (string) Postal code provided on order

estimated_shipping_cost
: (string) Retailers estimated cost of shipping

dropship_fee
: (string) Retailer provided drop shipping fee

per_order_fee
: (string) Retailer provided order fee

estimated_tax
: (string) Retailers estimated tax cost

retailer_provided_order_attributes
: (string) Array of retailer provided order attribute objects

retailer_provided_notes
: (string) Retailer provided notes

retailer_provided_line_item_attributes
: (string) Array of retailer provided line item objects
