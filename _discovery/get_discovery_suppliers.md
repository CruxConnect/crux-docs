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

recent : (int) Number of days. If specified, returns suppliers that have made their products available in the Discovery Catalog in the past 'recent' days.
//////////// Alternate: don't have recent filter; just sort by date_joined_discovery
//////////// Alternate: have 'recent' be a boolean with a fixed number of days (say, 100) as the 'recent' period not exposed to the API

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
- shipping_origin : Country from which SKUs are shipped. Sort: alphabetic by English name of country.
- date_joined_discovery : Date when the supplier made their products available in the Discovery Catalog. Sort: chronologic.
//////////// Alternate: don't have date_joined_discovery sort; just have 'recent' filter

dir : (string) Direction of sorting. Default: asc. Options are:
- asc : Ascending. alphabetic: 0 --> 9 --> A --> Z; numeric: 0 --> 9; chronologic: old --> new.
- desc : Descending. alphabetic: Z --> A --> 9 --> 0; numeric: 9 --> 0; chronologic: new --> old.
Any 'dir' that is a string but is not 'asc' is treated as 'desc'.
//////////// Do we have to specify both key and dir for it to work? If we give it sort: undefined it will provide a default key and dir; if we give it { key: number_of_skus } will it provide a default dir, use whatever the dir currently is, or give us an error message?
//////////// Is there one default dir used for all keys or does each key get its own default direction? That is, should it default 'fulfillment_percentage' to descending and 'shipping_origin' to ascending?

### Response Parameters:

uuid : (string) Universal Unique Identifier for the supplier

name : (string) Supplier name. Character case is specified, eg, "McCord Manufacturing" rather than "MCCORD MANUFACTURING". Maximum length is 200 characters. The name is encoded in UTF-8 and is not restricted to traditional English characters.
//////////// If the simplified/standardized supplier name is not the same as the actual name, which one do we display here?

website : (string) Browser-ready URL for supplier's public-facing website. A URL is 'browser-ready' if we can put it in an internet browser and the website loads.

description : (string) Summary, provided by the supplier, of what the supplier offers.
//////////// Should the length be constrained, say, 300 characters?

number_of_skus : (int) Number of SKUs that the supplier has made visible in the Discovery Catalog.
//////////// Is this the number of SKUs available in the discovery catalog, available in their regular catalog through Crux, something else?

fulfillment_percentage : (float) Percentage of SKUs ordered from the supplier through Crux that the supplier has delivered. At a minimum, the fulfillment_percentage will be calculated to at least two decimal places.
//////////// Is this the way want to calculate fulfillment? Alternate(s):
percentage of _orders_ marked 'delivered'
percentage of _orders_ marked 'Allocated' or 'HasTracking' (ie, not 'Backordered', 'Rejected', or 'Unallocated'; ignore retailer-initiated 'Cancelled').
percentage of _SKUs_ marked 'Allocated' or 'HasTracking' (ie, not 'Backordered', 'Rejected', or 'Unallocated'; ignore retailer-initiated 'Cancelled').

shipping_origin_country_name : (string) English name of country from which SKUs are shipped. The names come from the 'Country name' column of ISO 3166-1 alpha-2 without any change in capitalization. (Note: behind the scenes, Crux only identifies a country by its two-character ISO 3166-1 alpha-2 code. If there is every a discrepancy between the country code and the country name, the code takes precedence.)

contact : (object) See below. An individual employee of the supplier designated as the contact person for Crux-related questions.

Contact Object:
name : (string) Contact's name. Character case is specified, eg, "La'Quanda McCann" rather than "LA'QUANDA MCCANN". Maximum length is 200 characters. The name is encoded in UTF-8 and is not restricted to traditional English characters. Examples of valid names: "Daffy Duck", "Sūn Démíng (孫德明)", "Kawin Thamsatchanan (กวินทร์ ธรรมสัจจานันท์)", "René Just Haüy", "Sofía Rodríguez de la Peña y de Ybarra", "Håkon Jørgensen".

uuid : (string) Contact's user UUID.

email : (string) Contact's email address. Maximum length is 200 characters.

phone : (string) Contact's phone number. Maximum length is 20 characters.

