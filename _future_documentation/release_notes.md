---
title: Release Notes
position: 2
visibility: future
---

Following are the API Endpoints planned for future release:

### API Endpoints

##### New

* Supplier or Retailer - Get Orders Attributes: (POST) /orders/attributes/{order_uuid}
* Supplier - Create Invoices - (POST) /orders/{order_uuid}/invoices/
* Retailer - Get Invoices - (GET) /orders/{order_uuid}/invoices/
* Supplier or Retailer - Get Orders: (GET) /orders/
* Internal - Acknowledge Orders  (PATCH) /orders/acknowledge

##### Modified

* Retailer - Create Order: (POST) /orders/create
* Supplier - Allocate Order: (PUT) /orders/allocation/{order_uuid}
* Supplier - Add Order Tracking: (POST) /orders/tracking/{order_uuid}
* Supplier - Update Order Tracking: (PUT) /orders/tracking/{order_uuid}/{old_tracking_number}
* Supplier or Retailer - Get Orders Fees: (PATCH) /orders/fees/{order_uuid}

##### Depricated

None currently planned for this release
