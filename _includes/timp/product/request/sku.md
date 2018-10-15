item
: (object) The Item object contains the item_uuid; the item_uuid is the parent identifer for the sku_uuid.

sku_id
: (string) The SKU Identifier for the SKU as provided by the Supplier

restrictions
: (string) The Restrictions imposed on the SKU which can include "tmpunavail" (temporary unavailable) or "discontd" (dicontinued)

condition
: (string) The Condition of the SKU; these include "new", "used", and "refurb" (refurbished)

quantity_in_stock
: (integer) The Quantity In-Stock parameter indicates how many SKUs are currently available for purchase.

quantity_on_backorder
: (number) The Quantity on Backorder parameter indicates how many of this particular SKU are going to be replenished. It can be considered a tentative quantity to be added to the current quantity in-stock.

number_of_units_bundled
: (integer) The Number of Units Bundled parameter indicates how many SKUs are in a single bundle.

sku_distinguishing_attributes
: (array) Attributes that help to distinquish one sku from another. It may also be empty, as per the Suppliers' discretion. For example, the `color: blue` is a distinquishing attribute if another another sku of the same item is `color: green`

sku_nondistinguishing_attributes
: (array) Attributes that are particular to the individual sku and do not necessarily distinquish a sku from other skus. It may also be empty, as per the Suppliers' discretion.  For example, the `color: blue` is a non-distinquishing attribute if another sku(s) of the same item has the attribute `color: blue`.  If all the skus of an item share the same non-distinguishing attribute, then it is preferrable to list that attribute as part of `item_attributes`.

minimum_advertised_price
: (decimal) The Minimum Advertised Price (MAP) is a price floor for advertisement on the SKU. You may not legally list the SKU for sale at a lower price. (2 decmial places)

msrp
: (decimal) The Manufacturer's Suggested Retail Price for the SKU. This is only a suggestion. It is not a price floor nor is it a price ceiling. (2 decmial places)