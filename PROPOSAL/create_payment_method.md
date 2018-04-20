# Create Payment Method
## URI
`/billing/payment-methods/`

## Method
POST

## Request
```js
{
  source_token: 'string', // The Stripe token for the payment source
  payment_method_token: 'string', // The Stripe token for the payment method
  is_default: null, // Not required. Defaults to false
}
```

## Response
```js
{
  uuid: '2e923440-76ba-4821-b50c-4cd7b4c462c6',
}
```
201
