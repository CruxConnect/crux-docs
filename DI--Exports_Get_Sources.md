task-THAN-237: consider collapsing into Product--READ-InventoryList-SubCatalog.md

### URL

```
GET /data-integration/exports/sources
```

### Request
```
empty body
```

### Response

```
{
  sources: {
    <source_uuid>: {
      uuid: <string>,
      type: <string>,  // my_orders, catalog, sub_catalog, inventory_list
      name: <string>,  // eg, 'Inventory List Alpha', 'Weekly Report'
    },
    <source_uuid>: {
      ...,
    },
    ...,
  },
}
```
