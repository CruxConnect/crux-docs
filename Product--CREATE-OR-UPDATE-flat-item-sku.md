### URL

```
POST /products/flat-item-skus/
```

### Request

Accepts all fields described in "Product--thanos-import-format" as a single dict.

In general, if the field exists and an empty string or None is passed in, then
the value will be set to None (including any closely related information on
complex objects).  If the field is not present at all, then pre-existing data
will be preserved.

### Responses

#### Successful new submission

```js
status: 201 Created
{ ... the sku and item data }
```

#### Successful update

```js
status: 200 OK
{ ... the sku and item data }
```

#### Salvaged create/update

Submissions with bad data may be salvaged if the bad data is not critical to
the submission or update.  In this case, the object is updated with the good
data and a warning is returned indicating exactly what happened.

```js
status: 202 Accepted
{
    "warning": {
        "message": "Some fields contained bad data. Bad data was removed and remaining fields successfully submitted."
        "detail": {
            'isbn': ["Invalid ISBN 'B0052P23YY': Only numbers allowed."],
            'asin': ["Invalid ASIN '182741000850': Wrong length", "Ensure this field has no more than 10 characters."]
        }
    }
    "accepted": {
        ... the accepted sku data
    }
}
```

#### Failed create/update

```
status: 400 Bad Request
{
    bad_data: {
        "critical": salvage_serializer.errors
        "non_critical": serializer.errors - salvage_serializer.errors
    }
}
```
