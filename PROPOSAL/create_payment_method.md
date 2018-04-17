# Create Payment Method
## URI
`/billing/payment-methods/`

## Method
POST

## Request
```js
{
  payment_method_token: 'string', // The Stripe token for the payment method
  is_default: null, // Not required. Defaults to false
}
```

## Response
```js
```
201
