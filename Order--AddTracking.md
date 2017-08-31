###  URL

### 

POST /api/orders/tracking/\<order\_uuid\>/

### Request

(Required fields: `sku`, `quantity`)

```json
{
  "tracking": <string>,
  "ship_cost": <num>,
  "carrier": <string>,
  "method": <string>,
  "skus": [{
    "sku_id": "CHOCO77",
    "quantity": <num>
  }],
  "weight": <num>,
  "line_item_uuid": <uuid>,
}

```

### Response

```json
```

### Status Code: 
204 No Content

### Error Status Codes:
400 Bad Request