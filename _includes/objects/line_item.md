uuid
: (string) Universal Unique Identifier for the Line Item

status
: (string) The Status for the Line Item. Possible Values are: Unallocated, Allocated, Rejected, HasTracking, Backordered, Cancelled

item_uuid
: (string) Universal Unique Identifier for the Item

item_name
: (string) The Item Name

sku_uuid
: (string) The Univeral Unique Identifier for the SKU

sku_id
: (string) The SKU as provided by the Supplier

sku_name
: (string) The SKU Name

sku_title_variants
: (string) SKU title variants

sku_special_instructions
: (string) SKU special instructions

cost
: (decimal) The Cost of the SKU (2 decimal places)

supplier_uuid
: (string) The Universal Unique Identifier for the Supplier

supplier_name
: (string) The Supplier Name

tracking_numbers
: (array) The Tracking Numbers array parameter includes tracking number objects. Each include a tracking number, carrier, method, weight, cost, shipping date, and quantity.

allocation
: (object) The Allocation object contains quantity ordered, quantity allocated, quantity backordered, quantity rejected, and backorder date.