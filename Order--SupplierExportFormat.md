## Order Export format for a Supplier

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
o.order_uuid	
o.retailer_po_number	
o.supplier_po_number	
o.requested_shipping_carrier	
o.requested_shipping_method	
o.retailer_id	
oi.sku	
oi.quantity	
oi.price	
oa.name	
oa.address1	
oa.address2	
oa.city	
oa.state	
oa.postal_code	
oal.quantity_accepted	
oal.quantity_rejected	
oal.quantity_backordered	
oal.backorder_date	
of.estimated_shipping_cost	
of.dropship_fee	
of.per_order_fee	
of.estimated_tax	
p.tracking_number	
p.shipping_carrier	
p.shipping_method	
p.weight	
p.shipping_cost	
p.shipping_date
```