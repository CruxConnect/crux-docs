##### Sort Object:
key
: (string) Field on which to sort. Default: supplier. Options are:
- supplier : name of the supplier in English. Sort: alphabetic.
- number_of_skus : number of supplier's SKUs in the Discovery Catalog. Sort: numeric.
- fulfillment_percentage : percentage of SKUs ordered from the supplier that the supplier delivers. Sort: numeric.
- shipping_origin : Country from which SKUs are shipped. Sort: alphabetic by English name of country.

dir
: (string) Direction of sorting. Options are:
- asc : Ascending. alphabetic: 0 --> 9 --> A --> Z; numeric: 0 --> 9
- desc : Descending. alphabetic: Z --> A --> 9 --> 0; numeric: 9 --> 0
Any 'dir' that is a string but is not 'asc' is treated as 'desc'. The 'key' is required but 'dir' is optional. If no 'dir' is given, it defaults as follows:
- supplier : asc
- number_of_skus : desc
- fulfillment_percentage : desc
- shipping_origin : asc