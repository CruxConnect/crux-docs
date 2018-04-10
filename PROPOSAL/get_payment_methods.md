# Get Payment Methods
## URI
<!-- TODO -->

## Method
GET

## Request
```js
```

## Response
```js
[
  {
    "uuid": "payment-method-uuid",
    "type": "card", // one of ['card', 'bank_account']
    "address": {
      "city": null,
      "country": null,
      "line1": null,
      "line2": null,
      "state": null,
      "zip": null,
    },
    "brand": "Visa", // REQUIRED. one of American Express, Diners Club, Discover, JCB, MasterCard, UnionPay, Visa, or Unknown
    "exp_month": 8,
    "exp_year": 2019,
    "last4": "4242",
    "name": "Bob Barker",
    "is_default": false, // Required. boolean

    // These are N/A, so... null
    "bank_name": null,
  },
  {
    "uuid": "payment-method-uuid",
    "type": "bank_account", // one of ['card', 'bank_account']
    "brand": "Unknown", // REQUIRED. bank account, so give unknown
    "account": "acct_1032D82eZvKYlo2C",
    "name": "Jane Austen",
    "bank_name": "STRIPE TEST BANK",
    "last4": "4242",
    "is_default": true, // Required. boolean

    // These are N/A, so... null
    "address": {}, // No address, so give an empty object
    "exp_month": null,
    "exp_year": null,
  },
]
```
