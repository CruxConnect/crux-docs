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
      images_from_recently_added_items: [
        // returns no more than 4
        {
          uuid: <image-uuid>,
          url: <string>,
          width: <int>,
          height: <int>
      ]
      ?? What sku information is wanted / needed ??
    }
  ],
}
```

