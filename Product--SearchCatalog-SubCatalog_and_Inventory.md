### URL

```
POST /products/items/search/
```

For now, searching of specific inventory lists and catalogs will be done with
a filter (if uuids) or facets (if using a name).

### Request

```js
{
  search_term: <string>,
  filters: {
    cost_per_unit: { min: <num>, max: <num>},
    minimum_tier_quantity: { min: <num>, max: <num> },
    quantity_in_stock: { min: <num>, max: <num> },
  },
  facets: {
    supplier: [ <uuid>, <uuid>, ...],
    shipping_cost_type: [<uuid>, <uuid>, ...], // 'free', 'fixed', 'variable'
    shipping_origin_country: [<uuid>, <uuid>, ...], // Country Name in title case
    bundle_type: [<uuid>, <uuid>, ...],  // 'Single Unit', 'Case Pack'
    product_identifiers: [<uuid>, <uuid>, ...] // 'UPC', 'ASIN', 'EAN ... most official
    condition: [<uuid>, <uuid>, ...], // New, Used, Refurbished, ...
    inventory_lists: [<uuid>, <uuid>, ...],
    catalogs: [<uuid>, <uuid>, ...],
    categories: [<uuid>, ...], 
  },
  sort: [<string or dict>, ...], // string='field' or '-field', dict={'field': {"order": "asc", "mode": "avg"}}, sku and pricing accessed via dot notation like this 'skus.quantity_in_stock' and 'skus.price_tiers.minimum_tier_quantity'.  
  pagination: {
    start: <num>,
    limit: <num>,
  }
}
```

### Response

if request body is empty, then the backend will response will be based on
  - pagination: { start: 0, limit: 50, total_results: <equal to all items>}
  - sort: item.title, ascending
  - category: Root + one layer

```json
{
  items: [
    {
      uuid: <string>,
      item_id: <string>,
      title: <string>,  // was title
      product_images: [{ url: <string>, heigth: <num>, width: <num>}], // was image
      supplier: {
        uuid: <string>,
        name: <string>,
      }
      cost_range: { // was price_range
        min: <num>,
        max: <num>,
      },
      sku_count: <num>,
      included_sku_count: <num>,  // used in inventory list, can be 0 or not provided for catalog
      last_updated: <date>,
    },
    ...
  ],
  pagination: {
    start: <record num>
    limit: num
    total_item_count: <num>,
  },
  sort: [<str or dict>, ...] // whatever was passed in for sort or default
  facets: {
    supplier: [
      { uuid: <string>, name: <string>, count: <num>, selected: <bool>},
      ...
    ],
    shipping_cost_type: [
      { uuid: <string>, name: <string>, count: <num>, selected: <bool> },
      ...
    ],
    shipping_origin_country: [
      { uuid: <string>, name: <string>, count: <num>, selected: <bool> },
      ...
    ],
    bundle_type: [
      { uuid: <string>, name: <string>, count: <num>, selected: <bool> },
      ...
    ]
    product_identifiers: [
      { uuid: <string>, name: <string>, count: <num>, selected: <bool> },
      ...
    ]
    condition: [
      { uuid: <string>, name: <string>, count: <num>, selected: <bool> },
      ...
    ]
    inventory_lists: [
      { uuid: <string>, name: <string>, count: <num>, selected: <bool> },
      ...
    ]
    catalogs: [
      { uuid: <string>, name: <string>, count: <num>, selected: <bool> },
      ...
    ],

    categories: [ // breadcrumbs + one layer
      {
        uuid: <string>,
        name: <string>,
        children: [
          {
            uuid: <string>,
            name: <string>,
            children:[
              {
                uuid: <string>,
                name: <string>,
                count: <num>,
                children: null,
              },
              {
                uuid: <string>,
                name: <string>,
                count: <num>,
                children: null
              },
            ],
          },
        ],
      },
    ],
  }
}
```
