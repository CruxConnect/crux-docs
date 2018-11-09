---
title: Order
name:
position: 3
visibility: file-specs
method:
description: The order section relates to the retailer fields
right_code: |

---

#### fees (object)
_Retailer Fields_

estimated_shipping_cost
: (float) Estimated shipping cost for the Order

drop_ship_fee
: (float) Drop Ship Fee for the order

order_fee
: (float) The Order Fee charged for processing orders through Crux.

#### retailer (object)
_Retailer Fields_

name
: (string) Organization name within your Retailer account

uuid
: (string) Universal Unique Identifier for your Organization

user
: (object) User object contains your name and email

#### address (object)
_Retailer Fields_

name
: (string) Name associated with the Address

business_name
: (string) Business associated with the Address

address_line_1
: (string) First line of the Address

address_line_2
: (string) Second line of the Address. If an apartment or suite, that information should be entered in this parameter.

city
: (string) City associated with the Address

state
: (string) State associated with the Address

postal_code
: (string) Zip Code / Postal Code associated with the Address

phone_number
: (string) Phone number associated with the Address

#### requested_shipping (object)
_Retailer Fields_

shipping_carrier
: (string) Shipping Carrier to deliver the order

shipping_method
: (string) Shipping method used by the Shipping Carrier to deliver the order.