###  URL

### 

POST /api/orders/tracking/\<order\_uuid\>/

### Request

(Required fields: `tracking`, `line_item_uuids`)

```json
{
  "tracking": <string>,
  "ship_cost": <num>,
  "carrier": <string>,
  "method": <string>,
  "weight": <num>,
  "line_item_uuids": [{
    "line_item_uuid": <uuid>, 
    "quantity": <num>}, 
  }]
}

```

### Response

```json
```

### Status Code: 
204 No Content

### Error Status Codes:
400 Bad Request