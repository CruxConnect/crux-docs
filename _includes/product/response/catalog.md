uuid
: (string) Universal Unique Identifier for the Catalog

supplier
: (object) The Supplier object contains a supplier_uuid

skus
: (array) Array SKU objects containing a single sku_uuid each

num_skus
: (number) The total Number of SKUs per the Catalog

default_shipping_cost
: (number) The Default Shipping Cost parameter contains a Shipping Cost the Supplier determined to be the Default. If null or empty, the Supplier has a variable ship cost per the SKUs or a more sophisticated Shipping strategy.

default_handling_cost
: (number) The Default Handling Cost parameter contains a Handling Cost the Supplier determined to be the Default. If null or empty, the Supplier has a variable handling cost per the SKUs or a more sophisticated handling strategy.

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