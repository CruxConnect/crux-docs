### URLs

```
POST /products/inventory-lists/<inventory-list-uuid>/add-items
POST /products/inventory-lists/<inventory-list-uuid>/add-skus
POST /products/inventory-lists/<inventory-list-uuid>/add-items-by-search
```

### By Item UUID Request

```js
{
  item_uuids: [<uuid>, <uuid>, ...]
}
```

### By SKU UUID Request

```js
{
  sku_uuids: [<uuid>, <uuid>, ...]
}
```

### By Search Request

```js
{
  search_term: <string>,
  filters: {
    // See filters object on catalog search request
  },
}
```

### Response

```js
status: 200 level
```
