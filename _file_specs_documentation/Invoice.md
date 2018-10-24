---
title: Invoice
name:
position: 8
visibility: file-specs
method:
description: The country where the product was manufactured. Must be a 2-digit ISO country code.
right_code: |
  ~~~ bash
  SS
  ~~~
  {: title="2-digit ISO Country Code" }

  ~~~ bash
   [ISO Country Cody List]({http://www.nationsonline.org/oneworld/country_code_list.htm})
  ~~~
  {: title="ISO Country Code List" }
---

#### Invoice
_Supplier Fields_

supplier_provided_drop_ship_fee
: (float) Supplier provided dropship fee

supplier_provided_order_fee
: (float) Supplier provided order fee

supplier_provided_tax
: (float) Supplier provided tax

supplier_provided_order_total
: (float) Supplier provided order total

supplier_provided_shipping_cost
: (float) Supplier provided shipping cost

_Retailer Fields_

order_uuid
: (string) The Universal Unique Identifier for the order

retailer_provided_notes
: (string) Retailer provided notes

retailer_provided_order_attributes
: (object) Array of retail provided Order Attribute objects

line_items
: (object) Array of line item objects

invoice_number
: (string) ***Required*** Invoice number


