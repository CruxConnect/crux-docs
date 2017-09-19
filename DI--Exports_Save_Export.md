### URL

```
POST /data-integration/exports
```

### Request
```
{
  uuid: <string>,
  export_name: <string>, // display name
  source_type: <string>,  // my_orders, catalog, sub_catalog, inventory_list
  source_name: <string>,  // eg, 'Inventory List Alpha', 'Weekly Report'
  created: <date-time>,
  filters: [need to elaborate]
  skus [or items?]: [need to elaborate]  // only for type=my_orders
}
```

### Response

```
status: 200
```
