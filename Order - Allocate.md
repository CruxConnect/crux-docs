###  URL

### 

PUT /api/orders/allocation/\<order\_uuid\>/

### Request

Note: Must include all line items on order. accepted + rejected + backordered must = qty ordered

```json
{
  "1bd61535-6d16-4fba-8d4a-c34e7446b5cd": {
    "quantity_accepted": 0,
    "quantity_backordered": 1,
    "quantity_rejected": 0,
    "backorder_date": "2017-09-02T00:00:00-06:00"
  },
  "68a07be9-9ff8-4745-bc16-dba2ba36818f": {
    "quantity_accepted": 1,
    "quantity_backordered": 0,
    "quantity_rejected": 0,
    "backorder_date": null
  }
}

```

### Response

```json
status: 200 level
```

