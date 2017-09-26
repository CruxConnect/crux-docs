### URL

###

POST /api/orders/

### Request

```json
{
  "start": 0,
  "limit": 25,
  "filters": {
    "sort": {
      "key": "<date/total>",
      "dir": "<asc/desc>",
    },
    "status": "<status>",
    "term": ""
    "start_date": "2017-07-31T06:00:00.000Z",
    "end_date": "2017-08-03T06:00:00.000Z",
    "org_uuids": [
      "1d02a0d4-8a29-4c33-9407-12fe5620d423",
      "6f76ac15-ff24-4e76-b0ac-bd936af67748"
    ],
  }
}
```

### Response

```json
{
  "orders": [
    { ...see order detail },
    ...
  ],
  "total_results": <int>,
}
```

