# Get Payment History
## URI
/billing/payment-history/ <!-- TODO: verify -->

## Method
GET

## Request
```js
```

## Response
```js
[
  {
    "created": 1523382891,
    "description": "My first payment",
    "amount": 2000,
    "amount_refunded": 0,
    "currency": "usd",
    "paid": true,
    "refunded": false,
    "source": {}, // IMPORTANT: Same as a single source from get_payment_methods.md
  },
  {
    //...
  },
]
```
