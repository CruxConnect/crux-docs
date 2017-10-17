###  URL

###

POST /api/orders/fees/

### Request

(Required fields: `sku_id`, `quantity`)

```js
{
  skus: [
    {
      sku_id: <string>,
      quantity: <int>,
    },
    ...
  ],
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

```js
 {
  estimated_shipping_cost: 30,
  drop_ship_fee: 5,
  order_fee: .99,
}
```

### Status Code:
200 OK

### Error Status Codes:
400 Bad Request
