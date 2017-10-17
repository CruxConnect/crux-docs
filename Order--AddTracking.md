###  URL

###

POST /api/orders/tracking/\<order\_uuid\>/

### Request

(Required fields: `tracking`, `line_item_uuids`)

```js
{
  "tracking": <string>,
  "ship_cost": <num>,
  "carrier": <string>,
  "method": <string>,
  "weight": <num>,
  "line_items": [{
    "line_item_uuid": <uuid>,
    "quantity": <num>},
  }]
}

```

### Response

```js
```

### Status Code:
204 No Content

### Error Status Codes:
400 Bad Request
