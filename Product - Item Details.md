### 

### Changes to discuss:

1. URL

### URL

### 

GET /api/??????????/\<item\_uuid\>

### Request

```json
empty body
```

### Response

Note: inventory\_list is same as sub\_catalog

```json
{
  title: <string>,
  map: { min: <num>, max: <num> },
  msrp: { min: <num>, max: <num> },
  price: { min: <num>, max: <num> },
  item_id: <string>,
  images: [
    { url: <string>, height: <num>, width: <num> },
    ...
  ],
  inventory_lists: [ {uuid: <string>, name: <string> }, {uuid: <string>, name: <string> }, ... ],
  sub_catalogs: [ {uuid: <string>, name: <string> }, {uuid: <string>, name: <string> }, ... ],
  description: <string>,
  categories: [ {uuid: <string>, name: <string> }, {uuid: <string>, name: <string> }, ... ],
  manufacturer: <string>,
  brand: <string>,
  origin_country: <string>,
  shipping_origin: <string>,
  fba_certified: <bool>,
  marketplace_restrictions: <string>,
  warranty: <string>,
  return_policy: <string>,
  last_updated: <date>,
  supplier: {
    uuid: <string>,
    name: <string>,
    contact_name: <string>,
    contact_email: <string>,
  },
  custom_attributes: {
    { name: <string>, value: <string> },
    { name: <string>, value: <string> },
    ...
  },
  skus: [
    {
      uuid: <string>,
      title: <string>, // derived attribute name
      map: <num>,
      msrp: <num>,
        pricing: [
          { minimum_tier_quantity: <num>, cost: <num> },
          { minimum_tier_quantity: <num>, cost: <num> },
          ...
        ],
      images: [ // image list is ordered
        { url: <string>, height: <num>, width: <num> },
        ...
      ],
      quantity_in_stock: <num>,
      minimum_order: <num>,
      shipping_cost: <num>,
      measurements: {
        sku: {
          weight: <num>,
          length: <num>,
          height: <num>,
          width: <num>,
        },
        package: {
          weight: <num>,
          length: <num>,
          height: <num>,
          width: <num>,
        },
      },
      product_codes: [ // SKU ID -- ENSURE THIS IS FIRST
        { name: <string>, code: <string> },
        { name: <string>, code: <string> },
        { name: <string>, code: <string> },
        ...
      ],
      distinquishing_attributes: [
        { name: <string>, value: <string> },
        { name: <string>, value: <string> },
        ...
      ],
    },
    <sku...>,
  ]
}
```

