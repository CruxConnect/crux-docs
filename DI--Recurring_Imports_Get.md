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
  scheduled_imports: {
    <import_uuid>: <object; see below>,
    ...,
  },
  sort_order: [<import_uuid>, <import_uuid>, ...],
}
```

Each scheduled_import nested object has the same format as the Request for Create-Recurring-Import (with fields timing, source, last_edit, and uuid)
(currently: https://github.com/DobaTech/thanos-api-docs/blob/THAN-237-data-integration/DI--Recurring_Import_Create.md)
