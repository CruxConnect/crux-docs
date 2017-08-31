### Changes to discuss:

1. URL

### URL

### 

??????????

### Request

```json
empty body
```

### Response

```json
{
  lists: [
    {
      "name": <string>,
      "description": <string>,
      "date_created": <datestring>,
      "created_user": {
        "uuid": <uuid>,
        "name": <string>,
      },
      "date_last_modified": <datestring>,
      "last_modified_user": {
        "uuid": <uuid>,
        "name": <string>,
      },
      "num_skus": <int>,
    }
    <list>,<list>,...
  ],
}
```

