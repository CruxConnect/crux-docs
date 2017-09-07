###  URL

###

POST /api/order/create/

### Request

(Required fields: `skus`, `address`, `shipping_carrier`, `shipping_method`, `purchase_order_id`)
(Optional fields: `notes`)

```json
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
  purchase_order_id: <string>,
  notes: <string>,
}
```

### Response

```json
// same as order detail response
{
  uuid: <uuid>,
  status: <string>,
  created_date: <datestring>,
  is_allocated: <bool>,
  purchase_order_id: <string>,
  notes: <string>,
  fees: {
    shipping: <number>,
    order_fee: <number>,
  },
  retailer: {
    name: <string>,
    uuid: <uuid>,
    user: {
      name: <string>,
      email: <string>,
    }
  },
  address: {
    name: <string>,
    business_name: <string>,
    address1: <string>,
    address2: <string>,
    city: <string>,
    state: <string>,
    postal_code: <string>,
  },
  requested_shipping: {
    shipping_carrier: <string>,
    shipping_method: <string>,
  },
  line_items: [
    {
      uuid: <uuid>,
      sku_uuid: <uuid>,
      sku_id: <string>,
      sku_name: <string>,
      supplier_uuid: <uuid>,
      supplier_name: <string>,
      cost: <number>,
      tracking_numbers: [
        {
          tracking_number: <string>,
          shipping_carrier: <string>,
          shipping_method: <string>,
          shipping_weight: <string>,
          shipping_cost: <number>,
          shipping_date: <datestring>,
        },
        ...
      ],
      allocation: {
        quantity_ordered: <int>,
        quantity_allocated: <int>,
        quantity_backordered: <int>,
        quantity_rejected: <int>,
        backordered_date: <datestring>,
      },
    },
  ],
}

```
### Status Code:
201 Created

### Error Status Codes:
400 Bad Request