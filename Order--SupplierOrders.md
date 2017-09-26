###  URL

###

POST /api/orders/supplier/\<supplier\_uuid\>/?created_after=&created_before&

### Request

(Required fields: `created_after`, `created_before` Notes: Date format must be `%Y-%m-%d %H:%M:%S.%f`)

```json

```

### Response

```json
{
  "uuid": <string>,
  "status": <num>,
  "is_allocated": <boolean>,
  "purchase_order_id": <string>,
  "created_date": <datetime>,
  "notes": <string>,
  "fees": {
     "shipping": <money>,
     "order_fee": <money>
  },
  "retailer": {
    "name": <string>,
    "uuid": <string>,
    "user": <user>
  },
  "address": {
    "name": <string>,
    "business_name": <string>,
    "address1": <string>,
    "address2": <string>,
    "city": <string>,
    "state": <string>,
    "postal_code": <string>,
  },
  "requested_shipping": {
    "shipping_carrier": <string>,
    "shipping_method": <string>
  },
  "line_items": [{
    "line_item_uuid": <uuid>,
    "quantity": <num>},
  }]
}
```

### Status Code:
200

### Error Status Codes:
400 Bad Request
