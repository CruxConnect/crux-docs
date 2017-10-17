### URLs

```
POST /products/inventory-lists/<inventory-list-uuid>/remove-items
POST /products/inventory-lists/<inventory-list-uuid>/remove-skus
POST /products/inventory-lists/<inventory-list-uuid>/remove-items-by-search
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
See search request
```

### Response

```js
status: 200 level
```
