###  URL

### 

POST /api/order/fees/

### Request

```json
{
  (Required:)
  skus: [
    {
      sku_id: <string>,
      quantity: <int>,
    },
    ...
  ],
  (Optional:)
  address: {
    name: <string>,
    business_name: <string>,
    address1: <string>,
    address2: <string>,
    city: <string>,
    state: <string>,
    postal_code: <string>,
  }
  shipping_carrier: <string>,
  shipping_method: <string>,
}
```

### Response

```json
 {
  estimated_shipping_cost: 30,
  drop_ship_fee: 5,
  per_order_fee: .99,
}
```
