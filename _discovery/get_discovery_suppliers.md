---
title: /discovery/suppliers [Jeff might change this]
name: Discovery Supplier list
method: POST
description: A list of all suppliers available to you in the discovery catalog
right_code: |
  ~~~ json
  {
    "initial_character": "e",
    "limit": "40",
    "recent": "90",
    "sort": {
      "key": "number_of_skus",
      "dir": "desc",
    },
    "start": "3"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "suppliers": [
      {
        "uuid": "9b3314d7-a280-4ed4-bf5c-83e3c9b013c0",
        "name": "Romero Reapers",
        "contact": {
          "uuid": "2e0ecb7e-9426-4e66-a8a9-e69cd8c806c0",
          "name": "Georgie Porgie",
          "email": "gporgie@puddingandpie.com",
          "phone": "1-722-036-2568x9442"
        },
        "logo": "https://api.adorable.io/avatars/50/abott@adorable.png",
        "description": "Reapers, Ramblers, Rabbits, Wrenches, and Wrigglers",
        "fulfillment_percentage": "91.2345839",
        "number_of_skus": "347,523",
        "shipping_origin_country_name": "United Arab Emirates",
        "website": "www.google.com",
      },
      {
        "uuid": "45d9c4a6-0bf0-4fa6-95df-c421ddba16e5",
        "name": "Best Company Ever",
        "contact": {
          "uuid": "97fa8fdf-6b94-409e-a684-841d42605881",
          "name": "Missy Muffet",
          "email": "mmuffet@sitonatuffet.com",
          "phone": "1-335-897-4352x1947",
        },
        "logo": "https://api.adorable.io/avatars/50/abott@adorable.png",
        "description": "Best stuff, best services, bestness, betterness",
        "fulfillment_percentage": "80.00000000001",
        "number_of_skus": "3,326,000",
        "shipping_origin_country_name": "Åland Islands",
        "website": "https://www.wearehardtoreach.com",
      }
    ]
  }
  ~~~
  {: title="Response" }

---
### Request Parameters:

Required: none

Optional:
initial_character
: (string) First character of supplier name OR '#'. If a letter or number, only suppliers whose name starts with this character will be returned. If '#', suppliers whose name starts with any number (0-9) will be returned. Only the first character of the string will be considered. Letters and numbers must be from UTF-8 ranges 0030-0039 (0-9), 0041-005A (A-Z), or 0061-007A (a-z). Upper- and lower-case letters are treated the same. (Some suppliers have company names with characters not in the specified ranges, but when they join Crux they provide a simplified, standardized name that uses only the limited character set above. It is the simplified/standardized name that determines where a supplier appears in the initial_character search.) Strings with more th

limit
: (int) Number of suppliers displayed on a page; used for paginating results. Default: 50. Maximum: 100. Any 'limit' greater than the Maximum will be forced to the Maximum.

recent
: (int) Number of days. If specified, returns suppliers that have made their products available in the Discovery Catalog in the past 'recent' days.

sort
: (object) Field and order for sorting. See below.

start
: (int) Element number of the first supplier that will be displayed on a page. (The available suppliers are returned in an ordered list, numbered from 0 to Number-of-suppliers, with each supplier an element in the list.) Used for paginating results. Default: 0. If greater than or equal to the number of available suppliers, 'start' is forced to the Number-of-suppliers (which will yield zero results).

Sort Object:
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

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the supplier

name
: (string) Supplier name. Character case is specified, eg, "McCord Manufacturing" rather than "MCCORD MANUFACTURING". Maximum length is 200 characters. Characters must be from UTF-8 ranges 0030-0039 (0-9), 0041-005A (A-Z), or 0061-007A (a-z).

contact
: (object) See below. An individual employee of the supplier designated as the contact person for Crux-related questions.

logo
: (string) URL for Supplier Logo image.  Image should be 50px by 50px

description
: (string) Summary, provided by the supplier, of what the supplier offers. The length is unconstrained.

fulfillment_percentage
: (float) Percentage of SKUs ordered from the supplier through Crux that the supplier has delivered. At a minimum, the fulfillment_percentage will be calculated to at least two decimal places.

number_of_skus
: (int) Number of SKUs that the supplier has made visible in the Discovery Catalog.

pagination
: (object) The Pagination object parameter includes the total_count, start, and limit for your Search.

shipping_origin_country_name
: (string) English name of country from which SKUs are shipped. The names come from the 'Country name' column of ISO 3166-1 alpha-2 without any change in capitalization. (Note: behind the scenes, Crux only identifies a country by its two-character ISO 3166-1 alpha-2 code. If there is ever a discrepancy between the country code and the country name, the code takes precedence.)

website
: (string) Browser-ready URL for supplier's public-facing website. A URL is 'browser-ready' if we can put it in an internet browser and the website loads. (For some websites that means that the protocol needs to be specified, eg, 'https://www.awesome.com'; for others, the protocol is not required, eg, 'www.verycool.com'.)

Contact Object:
uuid
: (string) Contact's user UUID.

name
: (string) Contact's name ready for display. Character case is specified, eg, "La'Quanda McCann" rather than "LA'QUANDA MCCANN". Maximum length is 200 characters. The name is encoded in UTF-8 and is not restricted to traditional English characters. Examples of valid names: "Daffy Duck", "Sūn Démíng (孫德明)", "Kawin Thamsatchanan (กวินทร์ ธรรมสัจจานันท์)", "René Just Haüy", "Sofía Rodríguez de la Peña y de Ybarra", "Håkon Jørgensen".

email
: (string) Contact's email address. Maximum length is 200 characters.

phone
: (string) Contact's phone number. Maximum length is 20 characters.

#### Pagination Object:

total_count
: (number) The Total Count of results returned for this Search

start
: (number) The Start parameter indicates on which element of the list of results the pagination should begin.

limit
: (number) The Limit parameter indicates one which element of the list of results the pagination should end.
