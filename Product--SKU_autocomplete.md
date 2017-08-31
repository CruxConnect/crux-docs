### URL

GET /products/skus/search/

### Request

```json
{
  partial: <string>,
}
```

### Response

???? WHAT is the minimum amount that you actually need from this request??
???? If you only need basic information I can return it straight from
???? elasticsearch and this will be super fast.  If you make me return a whole
???? bunch of stuff, then I'll have to hit the DB and it won't be as quick

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

