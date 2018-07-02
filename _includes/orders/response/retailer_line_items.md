line_item_uuid
: (string) Line Item Unversal Unique Identifier

status
: (string) Line Item Status.  Possible Values are: Unallocated, Allocated, Rejected, HasTracking, Backordered, Cancelled

sent_to_supplier
: (boolean) Has order been sent to supplier. Possible values are: True or False

item_uuid
: (string) Universal Unique Identifier for the Item

item_name
: (string) The Item Name

sku_uuid
: (string) The Universal Unique Identifier for the SKU

sku_id
: (string) The SKU as provided by the Supplier

sku_name
: (string) The SKU Name

sku_title_variants
: (string) SKU title variants

product_code:
: (object) Product codes object containing UPCA, EAN13, ISBN, GTIN14, ASIN, MPN

retailer_line_item_instructions
: (string) Retailer line item instructions

retailer_provided_sku_cost
: (decimal) Retailer provided SKU cost (2 decimal places)

supplier
: (object) Supplier object containing the supplier uuid and organization name

supplier_line_item_instructions
: (string) Supplier line item instructions

supplier_provided_attributes
: (array) Array of supplier provided attribute objects

tracking
: (array) Array of tracking objects

allocation": {

}

line_item_designation
: (string) Line item designation

##### Product Code Object

{% include orders/product_codes.md %}

##### Supplier Object

uuid
: (string) Universal Unique Identifier for the Supplier

supplier_org_name
: (string) Supplier Organization Name

##### Supplier Provided Attributes Object

{% include orders/attributes.md %}

##### Tracking Object
{% include orders/tracking.md %}

##### Allocation Object

quantity_ordered
: (integer) Quantity Ordered

quantity_accepted
: (integer) Quantity accepted

quantity_rejected
: (integer) Quantity rejected

quantity_backordered
: (integer) Quantity backordered

backorder_date
: (string) Backordered Date (yyy-mm-dd)


