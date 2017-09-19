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
    timing: { ... },  // same as in Create-Recurring-Import
    source: <string>,  // same as in Create-Recurring-Import
    last_edit: <date-time in UTC>,
  },
  ...,
]
```
