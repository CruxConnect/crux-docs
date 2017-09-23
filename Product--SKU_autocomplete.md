### URL

```
POST /products/skus/search/completion/
```

### Request

```json
{
  partial: <string>, // the sku_id
}
```

### Response

For now, this does partial autocomplete matches only on the `sku_id` field.

By only returning information already indexed in elasticsearch, we can avoid
having to hit the DB again after searching elasticsearch.  That will keep this
endpoint very fast.

```json
{
  skus: [
    {
      uuid: <uuid>,
      sku_id: <string>,
      title: <string>,
      number_of_units_bundled: <num>, // basically case_pack info
      price_tiers: [
        { minimum_tier_quantity: <num>, cost: <num> },
        { minimum_tier_quantity: <num>, cost: <num> },
        ...
      ],
      product_images: [{ <image info> }, ...]
    },
    <sku>,<sku>,...
  ]
}
```

