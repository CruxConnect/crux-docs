### URL

GET /api/data/export/\<uuid\>/

### Request

```js
empty body
```

### Response

```js
{
  uuid: <export record uuid>,
  status: <enum(pending,complete,???),
  url: <string>,  // optional: if status is complete, returns URL; if not, url will be <null>
}
```

