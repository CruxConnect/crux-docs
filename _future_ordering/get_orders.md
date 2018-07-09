---
title: /orders/
name: Get Orders
position: 1.03
visibility: public
method: post
description: Get the Orders for your organization
right_code: |
  ~~~ json
  null
  ~~~
  {: title="Request" }

  ~~~ json
  null
  ~~~
  {: title="Response" }

---
Get Orders matching certain criteria for your organization. This may contain any or all of your orders: completed, incomplete, processing, etc.


### Request Parameters:

start
: (int) The Start is the number of which "Order" you would like to start. If no other filters are used, the default order, which is date created, is used. The default Start value is 0. If this filter is not included in your request, the default value is used.

limit
: (int) The Limit is the element number of "Order" in your Orders List where you would like your results to end. If you have 10 orders and you limit at 8 and start at 4, only orders 4, 5, 6, 7, and 8 are included in the results.

sort
: (object) The Sort object contains a Key to sort on and a Direction (dir) to sort in.

line_item_allocation_statuses
: (array) One or more line item statuses. Possible choices include: `Unallocated`, `Partial`, or `Allocated`

: (string) Line item status designation.  One of the following : `HasTracking`, `NeedsTracking`, `Backordered`, `Rejected`, `Cancelled`

start_date
: (string) The Start Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

end_date
: (string) The End Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

term
: (string) Term can be Order UUID, PO Number or SKU ID

org_uuids
: (array) An array of Organization Universal Unique Identifiers

##### Sort Object:

{% include objects/sort.md %}

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
