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
    "transaction_id": 'ch_1CHhFtKmavcDRtKFleffsX9i', // Stripes charge id
    "created": '2018-04-23T21:01:02+00:00',
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
