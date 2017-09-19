## This endpoint is no longer in MVP

### URL

```
GET /data-integration/exports/?sort_by=<sort_by>
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
    export_name: <string>, // display name
    source_type: <string>,  // my_orders, catalog, sub_catalog, inventory_list
    source_name: <string>,  // eg, 'Inventory List Alpha', 'Weekly Report'
    created: <date-time>,
  },
  ...,
]
```
