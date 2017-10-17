### URL

```
GET /products/inventory-lists/
GET /products/catalogs/
```

### Request

```js
empty body
```

### Response for Beta

```js
{
  [
    {
      "uuid": <string>,
      "name": <string>,
      "description": <string>,
      "created": <datestring>,
      "last_updated": <datestring>,
      "retailer": { uuid: <string retailer-uuid> } 
      "skus": [ <string sku-uuid>, ],
    },
  ],
}
```

### Response for After Beta

```js
{
  [
    {
      "uuid": <string>,
      "name": <string>,
      "description": <string>,
      "created": <datestring>,
      "created_by_user": {
        "uuid": <string user-uuid>,
        "name": <string>,
      },
      "last_updated": <datestring>,
      "last_updated_by_user": {
        "uuid": <string user-uuid>,
        "name": <string>,
      },
      "num_skus": <int>,
      images_from_recently_added_items: [  // returns no more than 4
        {
          uuid: <image-uuid>,
          url: <string>,
          width: <int>,
          height: <int>
        },
      ],
      "retailer": { uuid: <string retailer-uuid> } 
      "skus": [ <string sku-uuid>, ],  // consider removing
    }
  ],
}
```


