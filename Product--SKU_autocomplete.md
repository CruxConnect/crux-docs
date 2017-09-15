### URL

```
GET /products/skus/search/
```

### Request

```json
{
  partial: <string>,
}
```

### Response

By only returning information already indexed in elasticsearch, we can avoid
having to hit the DB again after searching elasticsearch.  That will keep this
endpoint very fast.

```json
{
  skus: [
    {
      uuid: <uuid>,
      sku_id: <string>,
      name: <string>,
      number_of_units_bundled: <num>, // basically case_pack info
      pricing: [
        { minimum_tier_quantity: <num>, cost: <num> },
        { minimum_tier_quantity: <num>, cost: <num> },
        ...
      ],
      images: [{ <image info> }, ...]
    },
    <sku>,<sku>,...
  ]
}
```

