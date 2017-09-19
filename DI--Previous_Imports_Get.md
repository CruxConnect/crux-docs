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
[
  {
    uuid: <string>,
    date_imported: <date-time>,
    file_name: <string>,
    imported_to: <string>,  // Catalog, My Orders, Sub-Catalog, Inventory List
    status: <string>,  // Successful, Pending, Failed [need to elaborate]
    failure_message: <string>,  // Corrupt File, Interrupted Connection [need to elaborate]
  },
  ...,
]
```
