## Order Import format for a Retailer

### Legend/Key
The source of the fields based on our data model

```
o = order
oi = order_item
oa = order_address
oal = order_allocation
of = order_fee
p = package
``` 

#### Fields

```
o.retailer_po_number	
o.requested_shipping_carrier	
o.requested_shipping_method	
oi.supplier	
oi.sku	
oi.quantity	
oi.price	
oa.name	
oa.address1	
oa.address2	
oa.city	
oa.state	
oa.postal_code	
of.estimated_shipping_cost	
of.dropship_fee	
of.per_order_fee	
of.estimated_tax
```