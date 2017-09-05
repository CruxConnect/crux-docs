### URL

###

GET /api/orders/

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
    { // as currently responding
      "uuid": "b34a7114-15f1-4876-9f71-ce44e2eb8e0e",
      "status": "NEW",
      "created_date": "2017-08-29T17:35:18.538858Z",
      "is_allocated": false,
      "purchase_order_id": "po-c5KvRnm4",
      "retailer_name": "projectthanos",
      "retailer_uuid": "b4e61258-afb2-43d0-9a3f-c0343ab2366b",
      "requested_shipping": {
        "shipping_carrier": "UPS",
        "shipping_method": "Ground"
      },
      "line_items": [
        {
          "uuid": "bd1df289-3493-426e-92ab-0bae41c27718",
          "sku_uuid": "9de70e82-9c56-4509-b0e3-f98335d2212a",
          "sku_id": "WONKYWILLA1",
          "supplier_uuid": "be178b34-ba38-46f2-ba41-181702972d0a",
          "supplier_name": "Abbott and Sons",
          "tracking_numbers": [
            {
              "tracking_number": "1234134134",
              "shipping_carrier": "UPS",
              "shipping_method": "Next Day",
              "shipping_weight": "6oz",
              "shipping_cost": "10.35",
              "shipping_date": "2017-08-31T15:30:04.944504"
            }
          ],
          "allocation": {
            "quantity_ordered": 1,
            "quantity_allocated": 1,
            "quantity_backordered": 1,
            "quantity_rejected": 1,
            "backordered_date": "2017-08-31"
          }
        },
        ...,
      ]
    },
    ...,
  ],
  "total_results": <int>,
}
```

