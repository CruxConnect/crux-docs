### URL

### 

POST /api/orders/export/

### By UUID Request

```json
{
  uuids: [<uuid>, <uuid>, ...]
}
```

### By Search Request

```json
// All are optional
{
    endDate: "2017-08-03T06:00:00.000Z",
    orgUUIDs: [<uuid>, <uuid>, ... ],
    sort: {
      key: <date/total>,
      dir: <asc/desc>,
    }
    startDate: "2017-07-31T06:00:00.000Z",
    status: <string (order status)>,
    term: <string>,
}
```

### Response

1. Create an \<Export\> Record
2. Create a catalog export file (all item/sku details in “thanos” format)
3. Put that file on s3
4. update the \<Export\> record with the s3 url and a status

```json
{
  uuid: <export record uuid>,
}
```

