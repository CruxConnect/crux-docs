### URL

```
GET /data-integration/imports
```

### Request

```
empty body
```

### Response

```
{
  previous_imports: {
    <import_uuid>: {
      date_imported: <date-time>,
      file_name: <string>,
      imported_to: <string>,  // Catalog, My Orders, Sub-Catalog, Inventory List
      status: <string>,  // Successful, Pending, Failed [need to elaborate]
      failure_message: <string>,  // Corrupt File, Interrupted Connection [need to elaborate]
      uuid: <string>,
    },
    <import_uuid> : {
      ...
    },
    ...,
  }
  sort_order: [<import_uuid>, <import_uuid>, ...],
}
```
