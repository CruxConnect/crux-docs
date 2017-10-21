The thanos product import specification file allows items (the item is the
parent) and skus (the sku is the child with variant attributes) to be imported
into thanos.  Each item may be associated with multiple skus.

The format is flat, meaning that the item level information will be duplicated
for each sku.  If item level information changes between its children skus,
the last line specifying the item level information will be used.

```
[N] => an integer

#######################
# item level info
#######################

    item_id CharField(256) [**REQUIRED**]
    title CharField(256) [**REQUIRED**]
    description text (max 65,535 chars)
    warranty text (max 65,535 chars)
    return_policy (max 65,535 chars)
    manufacturer CharField(128)
    brand CharField(128)
    country_of_origin (Valid 2 letter country code)
    shipping_origin_country (Valid 2 letter country code)
    categories (comma_separated uuids)
    restrict_from_marketplaces comma_separated('amazon, 'ebay', 'newegg', 'overstock', 'walmart')
    other_marketplace_restriction CharField(256)
    fba_certified (bool)

    custom_attribute.[N].name CharField(128)
    custom_attribute.[N].value CharField(256)
    custom_attribute.[N].type (one_of: str, int, float, bool)

    # duplicate urls across sku or item will reference the same ProductImage
    product_images_for_item (comma separated urls)

#######################
# sku level info
#######################

    sku_id CharField(256) [**REQUIRED**]
    // todo-jan31: consider longer words
    restrictions (one_of: 'tmpunavail', 'discontd')
    // todo-jan31: consider refurbished instead of refurb
    condition (one of: 'new', 'used', 'refurb')
    quantity_in_stock (int >= 0)
    quantity_on_backorder (int >= 0)
    number_of_units_bundled (int >= 1)
    minimum_advertised_price (float)
    msrp (float)

    # measurements
    weight (float [kg])
    length (float [meters])
    width (float [meters])
    height (float [meters])

    package_weight (float [kg])
    package_length (float [meters])
    package_width (float [meters])
    package_height (float [meters])

    # identifiers
    upca CharField(12)
    ean13 CharField(13)
    gtin14 CharField(14)
    isbn CharField(13)
    asin CharField(10)
    mpn CharField(128)


    distinguishing_attribute.[N].name CharField(128)
    distinguishing_attribute.[N].value CharField(256)
    distinguishing_attribute.[N].type (one_of: str, int, float, bool)

    # This will generate a new price tier for the specified catalog
    pricing.[N].catalog <uuid>
    pricing.[N].minimum_tier_quantity (int)
    pricing.[N].cost (float)
    pricing.[N].shipping_cost (float)
    pricing.[N].shipping_cost_is_estimate (bool)

    # duplicate urls across sku or item will reference the same ProductImage
    product_images_for_sku (comma separated urls) [in future will support uuids]

    catalogs (comma separated uuids) [**SUPPLIER-ONLY**]
    inventory_lists (comma separated uuids--export only) [**RETAILER-ONLY**, **EXPORT-ONLY**]
```
