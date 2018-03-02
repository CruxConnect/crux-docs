---
title: /discovery/suppliers
name: Discovery Supplier list
method: POST
description: A list of all suppliers available to you in the discovery catalog
---
### Request Parameters:

Required: none

Optional:
start : (int) Element number of the first supplier that will be displayed on a page; used for paginating results. Default: 0. If greater than or equal to the number of available suppliers, will be forced to the number of available supplier minus 25.
//////////// Alternate(s) for greater than max: return an error code OR default to 0.

//////////// Two approaches to limiting:
stop : (int) Element number of the last supplier that will be the displayed on a page. Used for paginating results. Default: start + 25.
limit_per_page : (int) Number of suppliers displayed on a page; used for paginating results. Default: 25.
//////////// If we give them the option of setting the last supplier on a page or the size of the page, should we impose a constraint? What if they say they want a million records on a page?

sort : (object) Field and order for sorting. See below.

initial_letter : (string) First letter of supplier name. If specified, only suppliers whose name starts with this letter will be returned. String can contain no more than one character. Must be 'in English', that is, from UTF-8 ranges 0041-005A, 0061-007A. Upper- and lower-case letters are treated the same. (Many suppliers have company names from languages other than English, but when they join Crux they provide an English-language name along with their actual name. It is the first letter of the English name that determines where a supplier appears in the initial_letter search.)
//////////// Alternate(s) for more than one char: return an error code for poorly formatted; take the first letter of whatever is provided
//////////// What about suppliers that do not have Latin-alphabet names?
//////////// How do accents and other marks affect the sorting? What if there is an accent/mark on the first letter?
//////////// What about suppliers that have numbers in the name?

Sort Object:
key : (string) Field on which to sort. Default: supplier. Options are:
- supplier : name of the supplier in English. Sort: alphabetic.
- number_of_skus : number of supplier's SKUs in the Discovery Catalog. Sort: numeric.
- fulfillment_percentage : percentage of SKUs ordered from the supplier that the supplier delivers. Sort: numeric.
- shipping_origin : Country from which SKUs are shipped. Sort: alphabetic.
- date_joined_discovery : Date when the supplier made their products available in the Discovery Catalog. Sort: chronologic.

dir : (string) Direction of sorting. Default: asc. Options are:
- asc : Ascending. alphabetic: A --> Z; numeric: 0 --> 9, 0% --> 100%; chronologic: old --> new.
- desc : Descending. alphabetic: Z --> A; numeric: 9 --> 0, 100% --> 0%; chronologic: new --> old.
Any string that is not 'asc' is forced to 'desc'.
//////////// Do we have to specify both key and dir for it to work? If we give it sort: undefined it will provide a default key and dir; if we give it { key: number_of_skus } will it provide a default dir, use whatever the dir currently is, or give us an error message?
//////////// Is there one default used for all keys or does each key get its own default direction? That is, should it default 'fulfillment_percentage' to descending and 'shipping_origin' to ascending?

### Response Parameters:

org_uuid
: (string) Universal Unique Identifier for the supplier

org_name
: (string) The name of the supplier

???
