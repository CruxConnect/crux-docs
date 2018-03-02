---
title: /discovery/suppliers
name: Discovery Supplier list
method: POST
description: A list of all suppliers available to you in the discovery catalog
---
### Request Parameters:

Required: none

Optional:
start : (int) Element number of the first supplier that will be displayed on a page. (The available suppliers are returned in an ordered list, numbered from 0 to Number-of-suppliers, with each supplier an element in the list.) Used for paginating results. Default: 0. If greater than or equal to the number of available suppliers, will be forced to the number of available supplier minus 50.
//////////// Alternate(s) for greater than max:
return an error code
default to 0
default to full last page (number_of_suppliers - 50, ie, start at last element and count back a full page)
default to normal last page (number_of_suppliers modulo 50, ie, if you started at 0 and clicked the 'last' button on the pagination bar)

limit : (int) Number of suppliers displayed on a page; used for paginating results. Default: 50. Maximum: 200.
//////////// Should we impose a constraint? What if they want a million records on a page?

sort : (object) Field and order for sorting. See below.

initial_character : (string) First character of supplier name OR '#'. If a letter or number, only suppliers whose name starts with this character will be returned. If '#', suppliers whose name starts with any number (0-9) will be returned. String can contain no more than one character. Letters and numbers must be from UTF-8 ranges 0030-0039 (0-9), 0041-005A (A-Z), or 0061-007A (a-z). Upper- and lower-case letters are treated the same. (Many suppliers have company names with characters not in the specified ranges, but when they join Crux they provide, along with their actual name, a simplified, standardized name that uses only the limited character set above. It is the simplified/standardized name that determines where a supplier appears in the initial_character search.)
//////////// Alternate(s) for more than one char:
return an error code;
take the first character of whatever is provided
take the first character of whatever is provided and return a warning

Sort Object:
key : (string) Field on which to sort. Default: supplier. Options are:
- supplier : name of the supplier in English. Sort: alphabetic.
- number_of_skus : number of supplier's SKUs in the Discovery Catalog. Sort: numeric.
- fulfillment_percentage : percentage of SKUs ordered from the supplier that the supplier delivers. Sort: numeric.
- shipping_origin : Country from which SKUs are shipped. Sort: alphabetic.
- date_joined_discovery : Date when the supplier made their products available in the Discovery Catalog. Sort: chronologic.

dir : (string) Direction of sorting. Default: asc. Options are:
- asc : Ascending. alphabetic: 0 --> 9 --> A --> Z; numeric: 0 --> 9; chronologic: old --> new.
- desc : Descending. alphabetic: Z --> A --> 9 --> 0; numeric: 9 --> 0; chronologic: new --> old.
Any 'dir' that is a string but is not 'asc' is treated as 'desc'.
//////////// Do we have to specify both key and dir for it to work? If we give it sort: undefined it will provide a default key and dir; if we give it { key: number_of_skus } will it provide a default dir, use whatever the dir currently is, or give us an error message?
//////////// Is there one default dir used for all keys or does each key get its own default direction? That is, should it default 'fulfillment_percentage' to descending and 'shipping_origin' to ascending?

### Response Parameters:

org_uuid
: (string) Universal Unique Identifier for the supplier

org_name
: (string) The name of the supplier

???
