## Order Import format for a Supplier

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
o.supplier_po_number	
oi.sku	
oi.quantity	oi.price	
oal.quantity_accepted	
oal.quantity_rejected	
oal.quantity_backordered	
oal.backorder_date	
of.dropship_fee	
of.per_order_fee	
of.estimated_tax	
p.tracking_number	
p.shipping_carrier	
p.shipping_method	
p.weight	
p.shipping_cost	p.shipping_date
```