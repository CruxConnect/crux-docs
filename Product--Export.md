### URL

```
GET /products/items/export/
GET /products/items/search/export/
```

### By Item UUID Request

```json
{
  uuids: [<uuid>, <uuid>, ...]
}

### By Search Request

See search request

If exporting inventory_list then provide it as parameter in inventory_list
facet.  Same with catalog.

### Response

1. Create an \<Export\> Record
2. Create a catalog export file (all item/sku details in “thanos” format)
3. Put that file on s3
4. update the \<Export\> record with the s3 url and a status

```json
{
  export: {
    uuid: <export record uuid>,
  }
}
```

