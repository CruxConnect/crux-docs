### URL

```
POST /products/inventory-lists/
POST /products/catalogs/
```

### Request

```js
{
  name: <string>,
  description: <string>,
  retailers: [<uuid>,<uuid>], // in the case of sub-catalog
}
```

### Response

```js
status: 200 level
```

