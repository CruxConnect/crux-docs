supplier
: (array) Array of suppliers using uuid or name

shipping_cost_type
: (array) Array of shipping costs types as defined by the Supplier

shipping_origin_country
: (array) Array of country shipping origins using the country codes using 2 character format. For example: "US", "CA", "GE"

bundle_type
: (array) Array of bundle types the Supplier has set up for the SKUs. Values for bundle_type_name include "Case Pack" and "Single".

product_identifiers
: (array) Array of product identifiers available on each SKU

categories
: (array) Array of categories in which SKUs may reside

catalog_type
: (array) Array of catalog types to which the retrieved SKUs belong.  Values include "standard" and/or "discovery".  Defaults to ["standard"] if catalog_type is not provided.
