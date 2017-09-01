### URL

GET /api/export/\<uuid\>/

### Request

```json
empty body
```

### Response

```json
{
  uuid: <export record uuid>,
  status: <enum(pending,complete,???),
  url: <string>,
}
```

