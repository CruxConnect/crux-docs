### URL

```
POST /products/items/search/
```

For now, searching of specific inventory lists and catalogs will be done with
a filter (if uuids) or facets (if using a name).

### Request

```json
{
  search_term: <string>,
  filters: {
    supplier_uuids: [<uuid>, <uuid>, ...],
    price: { min: <num>, max: <num>, type: ['bundle', 'unit']},
    minimum_tier_quantity: { min: <num>, max: <num> },
    shipping_cost_type: ['free', 'fixed', 'variable'],
    shipping_origin_country: [<2-letter-country-code>, ...],
    quantity_in_stock: { min: <num>, max: <num> },
    product_codes: {'name': ['value', ...]}, ...},
    category: <uuid>,  // Not yet available
  },
  // Any facet available in apps.products.search.item.ItemSearch
  // All possible values are implied in ItemSearch (need to fill in when we know)
  facets: {
    supplier_name: [<name>, <name>, ...],
    bundle_type: ['single', 'case_pack', ...],
    cost_per_unit: [<range name>, <range name>, ...]
    price_range: [as defined by ItemSearch'],
    condition: ['new', 'used', 'refurb'],
    inventory_lists: [name, name, ...],
    catalogs: [name, name, ...],
  }
  sort: [<string or dict>, ...], // string='field' or '-field', dict={'field': {"order": "asc", "mode": "avg"}}, sku and pricing accessed via dot notation like this 'skus.quantity_in_stock' and 'skus.price_tiers.minimum_tier_quantity'
  pagination: {
    start: <num>,
    limit: <num>,
  }
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
    supplier_name: {
      <name>: {
        count: <num>,
        selected: <bool>,
      }
      ...
    },
    // categories is not supported ATM
    categories: [ // breadcrumbs + one layer
      {
        name: <string>, // root
        children: [
          {
            name: <string>,
            children:[
              {
                name: <string>,
                count: <num>,
                children: null,
              },
              {
                name: <string>,
                count: <num>,
                children: null
              },
            ],
          },
        ],
      },
    ],
    price: {
      <name>: {
        count: <num>,
        selected: <bool>,
      },
      ...
    },
    shipping_cost: {
      <name>: {
        count: <num>,
        selected: <bool>,
      },
      ...
    },
    // Same pattern for all facets
    shipping_origin ...
    product_codes ...
    inventory_lists: {
      <name>: {
        count: <num>,
        selected: <bool>,
      },
      ...
    }
    catalogs: // same form as inventory_lists
  }
}
```
