### URL

GET /products/inventory-lists/
GET /products/catalogs/

### Request

```json
empty body
```

### Response

```json
{
  [
    {
      "uuid": <string>,
      "name": <string>,
      "description": <string>,
      "datetime_created": <datestring>,
      "created_by_user": {
        "uuid": <uuid>,
        "name": <string>,
      },
      "datetime_modified": <datestring>,
      "last_modified_by_user": {
        "uuid": <uuid>,
        "name": <string>,
      },
      "num_skus": <int>,
      ?? What sku information is wanted / needed ??
    }
  ],
}
```

