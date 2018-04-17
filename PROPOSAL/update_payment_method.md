# Update Payment Method
## URI
/something/<CARD_ID>/ <!-- TODO -->

## Method
PATCH

## Request
```js
{
  address: {
    "city": null,
    "country": null,
    "line1": null,
    "line2": null,
    "state": null,
    "zip": null,
  },
  "exp_month": 8,
  "exp_year": 2019,
  "name": "Carl Orf",
  "is_default": true,
}
```

## Response
```js
```
200? 202? 204? <!-- TODO -->
