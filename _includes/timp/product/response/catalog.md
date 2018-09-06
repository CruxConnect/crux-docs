uuid
: (string) Universal Unique Identifier for the Catalog

supplier
: (object) The Supplier object contains a supplier_uuid

skus
: (array) Array of SKU objects. SKU Objects are each composed of a single sku_uuid.

num_skus
: (integer) The total Number of SKUs per the Catalog

default_shipping_cost
: (decimal) The Default Shipping Cost parameter contains a Shipping Cost the Supplier determined to be the Default. If null or empty, the Supplier has a variable ship cost per the SKUs or a more sophisticated Shipping strategy. (2 decimal places)

default_handling_cost
: (decimal) The Default Handling Cost parameter contains a Handling Cost the Supplier determined to be the Default. If null or empty, the Supplier has a variable handling cost per the SKUs or a more sophisticated handling strategy. (2 decimal places)

retailer
: (object) The Retailer object contains a single retailer_uuid.

created
: (string) The Created parameter is the date the Catalog was Created.

last_updated
: (string) The Last Updated parameter is the date the Catalog was Last Updated.

name
: (string) The Name the supplier has designated for this Catalog

description
: (string) The Description the supplier has provided for this Catalog