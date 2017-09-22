###  URL

###

GET /api/notifications/

### Request

```json
{
  "start": 0,
  "limit": 10,
}
```

### Response

```json
[
  {
    "uuid": "<uuid>",
    "title": "<string>",
    "created_at": "2017-08-03T06:00:00.000Z",
    "type": "<string>", // enum, or no?
  },
]
```

### Status Code:
200 OK
