### Changes to discuss:

1. URL

### URL

### 

??????????



### By Item UUID Request

```json
{
  inventory_id: <uuid>,
  items: [<uuid>, <uuid>, ...]
}
```

### By SKU UUID Request

```json
{
  inventory_id: <uuid>,
  skus: [<uuid>, <uuid>, ...]
}
```

### By Search Request

```json
{
  inventory_id: <uuid>,
  search_term: <string>,
  filters: {
    // See filters object on catalog search request
  },
}
```

### Response

```json
status: 200 level
```

