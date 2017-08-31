### URL

???? I'm not 100% certain these URLs will not change ????

GET /products/items/?csv-export=true
GET /products/sku/?csv-export=true
GET /products/sku/search/?csv-export=true


### By Item UUID Request

```json
{
  items: [<uuid>, <uuid>, ...]
}

```

### By Sku UUID Request

```json
{
  skus: [<uuid>, <uuid>, ...]
}

```

### By Search Request

```json
{
  inventory_id: <uuid>,
  search_term: <string>,
  filters: {
    // See filters object on catalog search request
  },
}
```

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

