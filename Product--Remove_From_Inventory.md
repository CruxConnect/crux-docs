### URLs

```
POST /products/inventory-lists/<inventory-list-uuid>/remove-items
POST /products/inventory-lists/<inventory-list-uuid>/remove-skus
POST /products/inventory-lists/<inventory-list-uuid>/remove-skus-by-search
```

### By Item UUID Request

```json
{
  item_uuids: [<uuid>, <uuid>, ...]
}
```

### By SKU UUID Request

```json
{
  sku_uuids: [<uuid>, <uuid>, ...]
}
```

### By Search Request

```json
See search request
```

### Response

```json
status: 200 level
```
