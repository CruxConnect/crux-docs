### URL

```
GET /api/items/<item-uuid>
```

### Request

```json
empty body
```

### Response

Note: `inventory_list` is same as `sub_catalog`

```json
{
  title: <string>,
  minimum_advertised_price_range: { min: <num>, max: <num> },
  msrp_range: { min: <num>, max: <num> },
  cost_range: { min: <num>, max: <num> },
  item_id: <string>,
  images: [
    { url: <string>, height: <num>, width: <num> },
    ...
  ],
  description: <string>,
  categories: [ {uuid: <string>, name: <string> }, {uuid: <string>, name: <string> }, ... ],
  // todo-jan31: consider distributor?
  manufacturer: <string>,
  brand: <string>,
  origin_country: <string>,
  shipping_origin: <string>,
  fba_certified: <bool>,
  marketplace_restrictions: <string>,
  warranty: <string>,
  // todo-jan31: consider return_policy_category and standard policy types
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
      sku_id: <string>,
      // derived attribute name: "<distinguishing_att_values> | ... | <num_units>u | <condition>"
      // todo-oct31: title should remove anything that is redundant across all skus
      title: <string>, 
      // inventory_lists only returned for retailers
      inventory_lists: [ {uuid: <string>, name: <string> }, {uuid: <string>, name: <string> }, ... ],
      // catalogs only returned for suppliers
      catalogs: [ {uuid: <string>, name: <string> }, {uuid: <string>, name: <string> }, ... ],
      minimum_advertised_price: <num>,
      // todo-jan31: use full word 'refurbished'
      condition: (enum: new, used, refurb),
      msrp: <num>,
      price_scheme: {
        uuid: <uuid>,
        price_tiers: [
          { 
            minimum_tier_quantity: <num>,
            cost: <num>,
            shipping_cost: <num>,
            shipping_cost_is_estimate: <bool>
          },
          ...
        ],
      }
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
      product_codes: [
        // todo-jan31: consider breaking out isbn into isbn10 and isbn13
        { <name>: code <string> },
        { <name>: code <string> },
        { <name>: code <string> },
        ...
      ],
      distinquishing_attributes: [
        { <name>: <value> },
        { <name>: <value> },
        ...
      ],
    },
    <sku...>,
  ]
}
```
