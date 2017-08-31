###  URL

### 

POST /api/orders/tracking/\<order\_uuid\>/

### Request

```json
{
  "tracking": <string>,
  "ship_cost": <num>,
  "carrier": <string>,
  "method": <string>,
  "skus": {
    "CHOCO77": <num>,
    "WONKAWILLY1": <num>,
  },
  "weight": <num>,
  "line_item_uuid": <uuid>,
}

```

### Response

```json
status: 200 level
```

