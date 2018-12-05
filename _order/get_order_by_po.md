---
title: /timp/orders/po/&ltpo_number&gt/
name: Get Order Detail by PO Number
position: 4.01
visibility: internal
method: get
description: Get the Details for a specified Order by Retailer PO Number
right_code: |
  ~~~ json
  [
  {
    "order_uuid": "f7bc1028-844c-44ca-82df-fe76282d2a8b",
    "po_number": "po-5527771067",
    "created_date": "2018-08-23T16:07:35.864274Z",
    "address": {
      "name": "Bob Iger",
      "business_name": "NBC",
      "address1": "30 Rockefeller Plaza",
      "address2": "STE 123",
      "city": "New York",
      "state": "NY",
      "postal_code": "10112",
      "phone_number": "801-555-1212",
      "country": null
    },
    "sent_to_supplier": false,
    "retailer": {
      "uuid": "ebf3657c-2abb-4aff-be70-69082acc9302",
      "organization_name": "projectthanos",
      "order_submitted_by": null
    },
    "retailer_provided_order_notes": null,
    "supplier_provided_order_notes": null,
    "retailer_provided_fees": {
      "order_fee": 0.99,
      "order_tax": 2.97,
      "shipping_cost": 7.99,
      "dropship_fee": 0.5
    },
    "retailer_provided_order_attributes": null,
    "supplier_provided_order_attributes": null,
    "invoices": [
    {
      "invoice_items": [
        {
          "sku_id": "56",
          "quantity_ordered": 10,
          "quantity_invoiced": 6,
          "supplier_order_number": "third",
          "invoice_item_attributes": [
            {
              "attribute_name": "invoice item name",
              "attribute_value": "can't believe we need invoice item attribute names and values"
            }
          ]
        }
      ],
      "invoice_number": "abcdef-ghi",
      "invoice_attributes": [
        {
          "attribute_name": "invoice attribute name",
          "attribute_value": "invoice attribute value"
        }
      ]
    }
  ],
    "line_items": [
      {
        "line_item_uuid": "5e91d918-67e8-4957-a69a-df9d2072ad9b",
        "status": "Unallocated",
        "line_item_designation": null,
        "item_uuid": "3bb5ef3b-2f1e-41da-bd85-1d6c746b0fa8",
        "item_name": null,
        "sku_uuid": "841ca56b-26f8-4d45-ac25-5b40d1da7354",
        "sku_id": "7FZvMyg0BjfewNJJ",
        "sku_name": null,
        "sku_title_variants": "None {}",
        "product_codes": {
          "upca": null,
          "ean13": null,
          "isbn": null,
          "gtin14": null,
          "asin": null,
          "mpn": null
        },
        "supplier_item_notes": null,
        "retailer_item_notes": null,
        "retailer_provided_sku_cost": 27.2,
        "supplier": {
          "uuid": "d6ac857d-c844-4312-8485-6d121d065308",
          "organization_name": "Stevens, Smith and Krause",
          "order_submitted_by": null
        },
        "supplier_provided_item_attributes": null,
        "retailer_provided_item_attributes": [
          {
            "attribute_name": "donut",
            "attribute_value": "jelly"
          }
        ],
        "tracking": [
        {
          "tracking_number": "12345",
          "shipping_carrier": "UPS",
          "shipping_method": "Speedy Ground",
          "shipping_weight": null,
          "shipping_cost": 3,
          "shipping_date": "2018-11-12",
          "created_date": "2018-11-10T17:47:07.872391Z",
          "quantity": 10,
          "package_attributes": [
            {
              "attribute_name": "package attribute name",
              "attribute_value": "package attribute value"
            }
          ]
        }
      ],
        "allocation": null
      }
    ]
  }
  ]
  ~~~
  {: title="Response" }

---
Get the Details for a specified Order. This includes the identifiers for the order, universal unique identifier for the order, po number, SKU(s) ordered, and details on the destination, receiver, etc.

### URL Parameters

uuid
: (string) The Universal Unique Identifier for the Order