### Changes to discuss:

2. list\_id filter item

### URL

Search Items:
  GET /api/items/<item-uuid>/

Search Inventory List:
  GET /api/product/<item-uuid>/

### Request

```json
{
  filters: {
    supplier: [<uuid>, <uuid>, ...],
    category: <uuid>,
    price: { min: <num>, max: <num>},
    pricing_type: [<uuid>, <uuid>, ...],
    shipping_cost: [<uuid>, <uuid>, ...],
    shipping_origin: [<uuid>, <uuid>, ...],
    product_codes: [<uuid>, <uuid>, ...],
  },
  search_term: <string>,
  sort: <string>,
  start: <num>,
  limit: <num>,
}
```

### Response

```json
{
  items: [
    {
      uuid: <string>,
      item_id: <string>,
      name: <string>,
      image: <url>,
      supplier: {
        uuid: <string>,
        name: <string>,
      }
      price_range: {
        min: <num>,
        max: <num>,
      },
      sku_count: <num>,
      included_sku_count: <num>,  // Only for Inventory
      last_updated: <date>,
    },
    ...
  ],
  pagination: {
    start: <record num>
    limit: num
    total: num
  },
  sort: {
    key: 'key', // relevance, title, price, sku_variants, item_id, supplier, last_updated
    direction: <enum(asc/desc)>, // ascending, descending
  },
  filters: {
    list_id: <uuid>,
    supplier: [ // everything
      {
        uuid: <string>,
        name: <name>,
        item_count: <num>,
      }
    ],
    categories: [ // breadcrumbs + one layer
      {
        uuid: <string>, // root
        name: <string>,
        children: [
          {
            uuid: <string>,
            name: <string>,
            children:[
              {
                uuid: <string>,
                name: <string>,
                item_count: <num>,
                children: null,
              },
              {
                uuid: <string>,
                name: <string>,
                item_count: <num>,
                children: null
              },
            ],
          },
        ],
      },
    ],
    price: { // everything
      type: [
        {
          uuid: <string>,
          name: <string>,
          item_count: <num>
        }
      ],
      range: { // may display price range of shown items
        low: <num>,
        high: <num>,
      }
    },
    shipping_cost: [ // everything
      {
        uuid: <string>,
        name: <string>,
        item_count: <num>
      },
      ...
    ],
    shipping_origin: [ // everything
      {
        uuid: <string>,
        name: <string>,
        item_count: <num>,
      },
      ...
    ],
    product_codes: [ // everything
      {
        uuid: <string>,
        name: <string>,
        item_count: <num>,
      },
      ...
    ],
  }
}
```
