### URL

```
PATCH /products/inventory-lists/<inventory-list-uuid>
PATCH /products/catalogs/<catalog-uuid>
```

### Request

```js
{
  name: <string>,
  description: <string>,
  retailer_uuids: [<uuid>,<uuid>], // in the case of sub-catalog
}
```

### Response

```js
status: 200 level
```

