### URL

POST /products/inventory-lists/
POST /products/catalogs/

### Request

```json
{
  name: <string>,
  description: <string>,
  retailers: [<uuid>,<uuid>], // in the case of sub-catalog
}
```

### Response

```json
status: 200 level
```

