### URL

GET /api/??????????/\<uuid\>

### Request

```json
empty body
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

