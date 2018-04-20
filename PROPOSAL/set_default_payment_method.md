# Set Default Payment Method
Alternatively to this document we could simply use the update_payment_method call with a body of `{ is_default: true }`

## URI
`/billing/payment-methods/UUID

## Method
PATCH

## Request
```js
{
  "is_default": "True/False"
}
```

## Response
```js
```
204 No Content

## Error Response
404 Not Found
