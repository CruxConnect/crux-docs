# Update Payment Method
## URI
`/billing/payment-methods/UUID

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
204 No Content

## Error Response
404 Not Found
