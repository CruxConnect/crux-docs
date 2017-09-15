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
      number_of_units_bundled: <num>,  // i.e., case_pack info
      price_scheme: {
        // same as item detail
        uuid: <uuid>,
        price_tiers: [
          {
            minimum_tier_quantity: <num>,
            cost: <num>,
            shipping_cost: <num>,
            shipping_cost_is_estimate: <bool>
          },
          ...
        ]
      }
      images: [{ <image info> }, ...]
    },
    <sku>,<sku>,...
  ]
}
```

