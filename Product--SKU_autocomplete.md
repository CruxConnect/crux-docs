### URL

### 

??????????

### Request

```json
{
  partial: <string>,
}
```

### Response

```json
{
  skus: [
    {
      uuid: <uuid>,
      sku_id: <string>,
      name: <string>,
      qty_available: <int>,
      pricing: [
        // same as item detail
        { minimum_tier_quantity: <num>, cost: <num> },
        { minimum_tier_quantity: <num>, cost: <num> },
        ...
      ],
      image: <string>,
    },
    <sku>,<sku>,...
  ]
}
```

