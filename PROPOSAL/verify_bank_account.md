# Get Payment Methods
## URI
/billing/verify/<payment_method_uuid>/<!-- TODO -->

## Method
POST

## Request
```js
{
  amounts: [
    .23,
    .55,
  ],
}
```

## Response
```js
{
  "uuid": "payment-method-uuid",
  "status": 'verified', // Applies only to bank accounts. Use stripe's values

  // The rest of the bank account fields exactly as specified in the get_payment_methods call
  // ...
}
```

## Reponse Codes
<!-- TODO -->
400 - Verification Failed
