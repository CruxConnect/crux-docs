###  URL

###

PUT /api/orders/allocation/\<order\_uuid\>/

### Request

(Required fields: `line_items`)

Note: Must include all line items on order. accepted + rejected + backordered must = qty ordered

```json
{
  line_items: [
    {
      line_item_uuid: <uuid>,
      allocation: {
        "quantity_accepted": <int>,
        "quantity_backordered": <int>,
        "quantity_rejected": <int>,
        "backorder_date": <datetime>,
      },
    },
    ...
  ],
}
```

### Response

```json
status: 204 No Content
```

### Status Code:
204 No Content

### Error Status Codes:
404 Not Found