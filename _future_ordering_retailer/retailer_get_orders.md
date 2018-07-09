---
title: /orders/create/
name: Create Order
position: 1.00
visibility: future
method: post
description: Create an Order on your account
right_code: |
  ~~~ json
    null
  ~~~
  {: title="Request" }
---
Create an Order on your account. By providing the SKU(s), quantity ordered, destination, etc. you may create an order for fulfillment.


### Request Parameters:

skus
: (array) ***Required*** Array of SKU objects ordered

address
: (object) Business Address object

po_number
: (string) Purchase Order Number

retailer_provided_order_fee
: (decimal) Retailer provided order fee

retailer_provided_tax
: (decimal) Retailer provided tax

retailer_provided_shipping_cost
: (decimal) Retailer provided shipping cost

retailer_provided_drop_ship_fee
: (decimal) Retailer provided drop shipping fee

retailer_provided_order_attributes
: (array) Retailer provided order attribute array containing order attribute objects

retailer_provided_notes
: (string) Retailer provided notes


#### SKU Object:
<!-- task-github-127 can we starndize SKU objects -->

sku_id
: (string) ***Required*** The SKU ID is the SKU provided by the supplier which identifies that product you are purchasing

quantity
: (integer) ***Required*** The Quantity ordered of the SKU ID

supplier_org_uuid
: (string) ***Required*** The Supplier Identifier is the ID associated with the Supplier providing the SKU

retailer_provided_shipping_carrier
: (string) Retailer provided shipping carrier

retailer_provided_shipping_method
: (string) Retailer Provided shipping method

retailer_line_item_instructions
: (string) Retailer provided line item instructions

retailer_provided_sku_cost
: (decimal) Retailer provided sku cost

retailer_provided_line_item_attributes
: (array) Array of retailer provided line item attributes objects containing the attribute name and value

#### Address Object:

name
: (string) The Name associated with the Address

business_name
: (string) The Business Name associated with the Address

address1
: (string) The First line of the Address

address2
: (string) The Second line of the Address. If an apartment or suite, that information should be entered in this parameter.

city
: (string) The City associated with the Address

state
: (string) The State associated with the Address

postal_code
: (string) The Zip Code / Postal Code associated with the Address

country
: (string) The country associated with the Address

phone_number
: (string) The phone number associated with the Address

#### Order Attributes

{% include orders/attributes.md %}

#### Line Item Attributes

{% include orders/attributes.md %}

### Response Parameters:

order_uuid
: (string) The Universal Unique Identifier for the Order

po_number
: (string) The Purchase Order (PO) Number for this order. This is the one you provided in the request parameters. It is the Identifer that your organization uses to identify the Order.

created_date
: (string) The Date when the order was created. It will always be the same day as when you send in the request to Create the Order.

retailer_provided_notes
: (string) The notes you provided from your request to create the Order. Returns a Max length 250 characters

retailer
: (object) The Retailer object contains an organization name, organization uuid, and a user object

address
: (object) The Address object containing name, business name, address line 1, address line 2, city, state, postal code

retailer_provided_shipping
: (object) Retailer provided shipping object contains the shipping carrier and shipping method from the request to create the Order.

retailer_provided_fees
: (object) The Retailer Provided Fees object contains the estimated shipping cost, drop ship fee, order fee, and order tax

retailer_provided_attributes
: (array) Arraty of Retailer Provided Attribute Objects containing the attribute name and value

invoice
: (object) Invoice object containing the supplier order number, invoice number, and invoice items object

line_items
: (array) The Line Items contains line items with their uuid, item uuid, item name, sku uuid, sku id, sku name, cost, supplier uuid, supplier name, tracking numbers list, and allocation object.


#### Retailer Object:

uuid
: (string) The Universal Unique Identifier for your Organization

retailer_org_name
: (string) The Organization Name within your Retailer account

submitted_by_user
: (string) The name of the user who submitted the order

#### Address Object:

{% include objects/address_business.md %}

#### Retailer Provided Fees Object:

{% include orders/response/retailer_fees.md %}

#### Attributes Object

{% include orders/attributes.md %}

#### Invoice Object

supplier_order_number
: (string) Supplier Order Number

invoice_number
: (string) Invoice Number

invoice_items
: (object) Invoice Items containing the sku id, quantity ordered, quantity invoiced


##### Invoice Items Object

sku_id
: (string) SKU ID

quantity_ordered
: (integer) Quantity ordered

quantity_invoiced
: (integer) Quantity invoiced

#### Requested Shipping Object:

shipping_carrier
: (string) The Shipping Carrier to deliver the order

shipping_method
: (string) The Shipping Method used by the Shipping Carrier to deliver the order

#### Line Item Object:

uuid
: (string) Universal Unique Identifier for the Line Item

status
: (string) The Status for the Line Item. Possible Values are: Unallocated, Allocated, Rejected, HasTracking, Backordered, Cancelled

item_uuid
: (string) Universal Unique Identifier for the Item

item_name
: (string) The Item Name

sku_uuid
: (string) The Universal Unique Identifier for the SKU

sku_id
: (string) The SKU as provided by the Supplier

sku_name
: (string) The SKU Name

sku_title_variants
: (string) SKU title variants

line_item_special_instructions
: (string) SKU special instructions

cost
: (decimal) The Cost of the SKU (2 decimal places)

supplier_uuid
: (string) The Universal Unique Identifier for the Supplier

supplier_name
: (string) The Supplier Name

tracking_numbers
: (array) The Tracking Numbers array parameter includes tracking number objects. Each include a tracking number, carrier, method, weight, cost, shipping date, and quantity.

allocation
: (object) The Allocation object contains quantity ordered, quantity allocated, quantity backordered, quantity rejected, and backorder date.

#### Tracking Numbers Object:

tracking
: (string) ***Required*** The Tracking number for the entire Order or a portion of the Order

supplier_provided_carrier
: (string) The Shipping Carrier who provided the Tracking Number

supplier_provided_method
: (string) The Shipping Method associated with the Tracking Number

package_weight
: (decimal) The Shipping Weight in pounds (lbs.) (2 decimal places)

package_ship_cost
: (decimal) The Shipping Cost for the entire Order or a portion of the Order as per the tracking  (2 decimal places)

package_ship_date
: (string) Package ship date

line_items
: (array) Line Items contains an array of Line Item objects containing line_item_uuid and quantity

### Expected Response Codes

{% include links/response_codes.md %}
