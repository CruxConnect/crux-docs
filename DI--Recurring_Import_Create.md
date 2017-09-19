### URL

```
POST /data-integration/imports
```

### Request

```
{
  timing: {
    entries: [<entry>, <entry>, ...] // Required; see below
    major_frequency: <string> // Required; one of: Year, Month, Week, Day, Hour
    hour: <string integer, 0-23>,
    minute: <string integer, multiples of 5, 0-55>,
    weekday_start: <string integer, 1-7>,
    weekday_stop: <string integer, 1-7>,
    hour_start: <string integer>, 0-22,
    hour_stop: <string integer>, 1-23,
  },
  source: <string>,
}
```

Entries will contain only objects of one of the following:

```{ month: <string integer, 1-12>, day: <string integer, 1-31> }```

```{ day: <string integer, 1-28> }```

```{ weekday: <string integer, 1-7> }```

```{ hour: <string integer, 0-23>, minute: <string integer, multiples of 5, 0-55> }```

```{ minute: <string integer, multiples of 5, 0-55> }```

In theory, the UI prevents the user from entering any values that don't match the
constraints above as well as preventing any non-calendrical values like Feb 30.

### Response

```
status: 200
```
