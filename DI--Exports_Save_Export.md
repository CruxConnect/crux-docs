### URL

```
POST /data-integration/exports
```

### Request
```
{
  export_name: <string>, // display name
  source_type: <string>,  // my_orders, catalog, sub_catalog, inventory_list
  source_uuid: <string>,
  filters: [same as the Order and Product 'Search' filters/search-term/list-ID (found in their respective docs)]
}
```

### Response

```
status: 200
```
