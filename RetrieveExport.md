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
  url: <string>,  // optional: if status is complete, returns URL; if not, url will be <null>
}
```

