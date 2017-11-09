---
title: /api/orders/
name: Get Order List
position: 3.00
type: post
description: Get the Order List for your organization
right_code: |
  ~~~ json
  {
    "start": 0,
    "limit": 25,
    "sort": {
      "key": "uuid",
      "dir": "des"
    },
    "status": "New",
    "start_date": "2017-07-31T06:00:00.000Z",
    "end_date": "2018-08-03T06:00:00.000Z"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "total_results": 28,
    "orders": [
      {
        "uuid": "299fc593-04f0-424d-9847-e359b9dfde56",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "bb1e6b18-25fa-4703-8ecb-c4c55da56086",
        "created_date": "2017-10-23T18:29:24.716079Z",
        "notes": "Blanditiis dolores maiores eveniet saepe at.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "James Smith",
          "business_name": "Price-Lloyd",
          "address1": "1878 Randy Valleys\nAnthonybury, OH 51137",
          "address2": "127 Cox Spurs\nLake Deborah, PW 48750",
          "city": "Lake Coltonstad",
          "state": "Ohio",
          "postal_code": "90181"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "abe537ad-d1ee-485e-8f60-920cbd9ba160",
            "item_uuid": "358d6043-220f-4107-93b7-1c22151dd5f0",
            "item_name": "The infamous blood item",
            "sku_uuid": "c3786845-3f06-4a10-a6cd-ff23461ab11f",
            "sku_id": "yl3t2Lij7XJfAnsB",
            "sku_name": "The infamous blood item",
            "cost": 58.16,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 6,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "a3efa8a0-c3ef-4dc1-81cc-07a6c5a57e2b",
            "item_uuid": "97fa8fdf-6b94-409e-a684-841d42605881",
            "item_name": "The changeable soap item",
            "sku_uuid": "f0b82bb2-0b12-42bf-b7e4-7195ccfb21ab",
            "sku_id": "utmcbyzttt",
            "sku_name": "The changeable soap item",
            "cost": 49.96,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 9,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "7c997127-19bd-430a-9f61-fdc49fc1527c",
            "item_uuid": "31adb57c-a40a-4a99-b3d0-3c6ccd8e8941",
            "item_name": "The cautious knowledge item",
            "sku_uuid": "9060814c-9feb-4a3e-958c-cb26d537cffc",
            "sku_id": "voGDR4gOyYUOgcT7gw",
            "sku_name": "The cautious knowledge item",
            "cost": 2.84,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 10,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "32012bb6-a580-41b7-b1f4-c9f62ced6bc9",
            "item_uuid": "98eb1720-9b1e-49ca-be08-e516e8fb46de",
            "item_name": "The aboard invention item",
            "sku_uuid": "dd9689e9-8241-4a78-afa1-7cbce9b09513",
            "sku_id": "BJA9PlgxiT9kQRaYUMF",
            "sku_name": "The aboard invention item",
            "cost": 96.49,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 1,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "713ddf6b-1f85-4ce5-86ff-bf6619bf82b4",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "60c34b21-cf25-421d-ab5a-bfe39b0122a6",
        "created_date": "2017-10-23T18:29:24.897608Z",
        "notes": "Sit nihil deleniti quam illum magnam aperiam dolor.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Emily Greene",
          "business_name": "Wilson Ltd",
          "address1": "Unit 5793 Box 1065\nDPO AP 43179",
          "address2": "606 Stevens Vista Suite 652\nLake Tonyaville, MI 68484-5519",
          "city": "New Jeffreyburgh",
          "state": "Louisiana",
          "postal_code": "50215"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "8e718458-2888-4268-9f40-97cfbc79bd46",
            "item_uuid": "db6537cc-7e4e-4d98-b7e6-7f9044d9de54",
            "item_name": "The enraged destruction item",
            "sku_uuid": "ec26763f-5395-47b7-b7bb-f0ce03058e1d",
            "sku_id": "USaoDXIiLNHOgNy",
            "sku_name": "The enraged destruction item",
            "cost": 12.32,
            "supplier_uuid": "0e9dd1c1-1eb5-45dc-9bb0-fe3d53f9da0d",
            "supplier_name": "Sharp, Green and West",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 3,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "0b62f1b1-a656-46eb-8d8e-4370174bb1c3",
            "item_uuid": "0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017",
            "item_name": "The capital arch item",
            "sku_uuid": "0cf678be-7dd1-47e3-852c-e80942d5566b",
            "sku_id": "UfvfG2",
            "sku_name": "The capital arch item",
            "cost": 33.16,
            "supplier_uuid": "1b348539-1f1a-432e-a9c3-63f71e65ad84",
            "supplier_name": "Underwood-Chavez",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 3,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "f44c2907-ade2-4a6e-b235-432036981c5e",
            "item_uuid": "9bd1c686-0ce1-404c-8055-d52e99e2a987",
            "item_name": "The enraged water item",
            "sku_uuid": "31ce0d04-e164-481e-9e41-82c4dff09aac",
            "sku_id": "fic0Sk",
            "sku_name": "The enraged water item",
            "cost": 47.23,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 7,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "1e3f529b-7046-457a-9b51-34cee7711b00",
            "item_uuid": "8e1898de-4bee-46ef-b242-16ddfacfd350",
            "item_name": "The innocent competition item",
            "sku_uuid": "260a181a-331e-4e4f-9a57-510048a5d3f2",
            "sku_id": "bpSH45MO",
            "sku_name": "The innocent competition item",
            "cost": 46.53,
            "supplier_uuid": "62bd2059-2f70-4cd5-9944-ba9969fe5f06",
            "supplier_name": "projectzuul",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 5,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "3a655157-5c23-4742-a0db-0afc9cfa4df6",
            "item_uuid": "8e1898de-4bee-46ef-b242-16ddfacfd350",
            "item_name": "The innocent competition item",
            "sku_uuid": "cffa8102-51d5-4b6a-a847-15ecd542840c",
            "sku_id": "0EdHRMyBgv5sI",
            "sku_name": "The innocent competition item",
            "cost": 18.98,
            "supplier_uuid": "62bd2059-2f70-4cd5-9944-ba9969fe5f06",
            "supplier_name": "projectzuul",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 9,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "de742b48-9a66-49b5-90ca-e7ad5f7c97e4",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "64d42d01-33ef-4ee2-ade1-ce3d581eee6c",
        "created_date": "2017-10-23T18:29:25.120938Z",
        "notes": "Pariatur quidem odio animi deleniti.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Dylan Simmons",
          "business_name": "Gentry, Thomas and Sloan",
          "address1": "4372 Scott Ranch Suite 626\nTravisborough, CT 32091",
          "address2": "25885 Randy Ways\nMollyfort, OR 78898-2675",
          "city": "Brownview",
          "state": "Washington",
          "postal_code": "27396"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "37d4fd2d-9e92-4198-b24a-5bab45f3f61a",
            "item_uuid": "32ef4bba-1332-4ad2-a599-84fd96be44e5",
            "item_name": "The incomparable arch item",
            "sku_uuid": "94d6d1ed-60d4-4f83-9474-f0fb9c8f6317",
            "sku_id": "LsPsWXJb",
            "sku_name": "The incomparable arch item",
            "cost": 77.1,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 8,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "ccd89da0-0258-404b-acb4-e27801f855cd",
            "item_uuid": "89cb0ff0-f524-4bc0-b247-09823cd8c4cc",
            "item_name": "The abnormal cause item",
            "sku_uuid": "9900924d-809e-4430-a863-afd6e7f5e71b",
            "sku_id": "e0l80mJfl47",
            "sku_name": "The abnormal cause item",
            "cost": 57.94,
            "supplier_uuid": "0e9dd1c1-1eb5-45dc-9bb0-fe3d53f9da0d",
            "supplier_name": "Sharp, Green and West",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 2,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "f13dae38-8483-4bc2-ab02-20cb851eb347",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "3918a246-519c-4015-aa21-10aaab38d08e",
        "created_date": "2017-10-23T18:29:25.378309Z",
        "notes": "Reiciendis inventore ratione neque placeat velit voluptatibus.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Joseph Pope",
          "business_name": "Meyers, Harris and Savage",
          "address1": "3808 Jonathan Burgs Apt. 708\nLopezville, GU 42809",
          "address2": "42442 Victoria Station\nLake Walterburgh, OR 37302-4510",
          "city": "Andrewsfurt",
          "state": "Idaho",
          "postal_code": "47170"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "fd80e88f-4677-49a9-8839-3862851af9d6",
            "item_uuid": "31adb57c-a40a-4a99-b3d0-3c6ccd8e8941",
            "item_name": "The cautious knowledge item",
            "sku_uuid": "9060814c-9feb-4a3e-958c-cb26d537cffc",
            "sku_id": "voGDR4gOyYUOgcT7gw",
            "sku_name": "The cautious knowledge item",
            "cost": 69.46,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 1,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "71a0cac0-022d-4732-af87-6e791b7ead6c",
            "item_uuid": "0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017",
            "item_name": "The capital arch item",
            "sku_uuid": "a81dc78b-6af2-461c-8a26-6e8d8a3e8b46",
            "sku_id": "KzQRPs",
            "sku_name": "The capital arch item",
            "cost": 15.45,
            "supplier_uuid": "1b348539-1f1a-432e-a9c3-63f71e65ad84",
            "supplier_name": "Underwood-Chavez",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 1,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "35251f9a-11a5-460d-bd5f-2ec3aaf6420c",
            "item_uuid": "d2563eb4-731b-478f-ba2e-194e323bce01",
            "item_name": "The chemical team item",
            "sku_uuid": "f99affa5-2e7f-4030-a23f-2cac7e6f6c28",
            "sku_id": "cIffdOE8Yr",
            "sku_name": "The chemical team item",
            "cost": 91.17,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 6,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "bcaed243-3a9b-4c3e-820e-66306764d49f",
            "item_uuid": "97fa8fdf-6b94-409e-a684-841d42605881",
            "item_name": "The changeable soap item",
            "sku_uuid": "5bd06e80-64ae-4150-bff9-fd3b8896c41c",
            "sku_id": "86EJwyYolPHU",
            "sku_name": "The changeable soap item",
            "cost": 94.74,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 9,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "4792dd1c-3b48-45a6-bbf7-573ff0237a9c",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "11ad8d3d-3fc7-4eb7-888e-c6a173a6dc71",
        "created_date": "2017-10-23T18:29:25.591136Z",
        "notes": "Expedita praesentium eaque nobis magnam.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Raymond Garrison",
          "business_name": "Solomon-Carlson",
          "address1": "04412 Robert View\nPort Scott, AK 58466",
          "address2": "PSC 2325, Box 7324\nAPO AA 49710",
          "city": "East Aprilburgh",
          "state": "Iowa",
          "postal_code": "42476"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "39f8317d-8f88-4609-b6eb-17c4526f5b3e",
            "item_uuid": "31adb57c-a40a-4a99-b3d0-3c6ccd8e8941",
            "item_name": "The cautious knowledge item",
            "sku_uuid": "1ba7a1e7-0eb3-46ae-875f-67d65caa94fa",
            "sku_id": "ok8AM531hs",
            "sku_name": "The cautious knowledge item",
            "cost": 91.72,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 10,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "5360ae67-e69b-4995-b91c-858ef5b8f94c",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "4a9f24bb-347f-4905-abec-1887f2f618b6",
        "created_date": "2017-10-23T18:29:25.702985Z",
        "notes": "Occaecati odio earum quas velit amet aperiam nisi.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Peter Robinson",
          "business_name": "Mclean, Trujillo and Lyons",
          "address1": "0158 Heather Lodge Suite 477\nFrankberg, NV 75210-5516",
          "address2": "684 Lauren Springs\nSouth Anthonystad, ND 86241-7551",
          "city": "Turnerhaven",
          "state": "Kentucky",
          "postal_code": "88212"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "86c6b47c-0b2e-4c64-b1c4-221be90dfe37",
            "item_uuid": "fffa059b-a4c7-4cac-a288-2a55534c170f",
            "item_name": "The insignificant drawer item",
            "sku_uuid": "a1258298-779a-421c-9f1b-fce82785a5e5",
            "sku_id": "rQwjZr",
            "sku_name": "The insignificant drawer item",
            "cost": 46.15,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 9,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "38134d80-fe5b-4628-81bd-d0a33b30c128",
            "item_uuid": "c23c72c4-91d6-492b-9a9b-3738b2e4fd1e",
            "item_name": "The embellished card item",
            "sku_uuid": "80588a81-fdc5-41bf-85ae-431d923f0d8d",
            "sku_id": "QyTsBbEK8Y5fYzee",
            "sku_name": "The embellished card item",
            "cost": 33.11,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 8,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "a01d57a7-453d-49c8-8bf1-d95885418d2d",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "5c85adb8-3257-4c67-b1cd-73464518f329",
        "created_date": "2017-10-23T18:29:25.844187Z",
        "notes": "In enim blanditiis sit eligendi.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Sean Jackson",
          "business_name": "Kim-Graham",
          "address1": "2552 Jill Cliffs\nLake Angela, WV 92974-8628",
          "address2": "579 Berry Hill Suite 035\nLake Elizabethchester, FM 02420-8210",
          "city": "South Christina",
          "state": "Massachusetts",
          "postal_code": "90548"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "4807115f-3f64-4138-a020-71772b2582b6",
            "item_uuid": "a0acc09b-bbfb-4087-a1ef-8201286980f8",
            "item_name": "The educated office item",
            "sku_uuid": "63ca88d9-91e2-4bd8-8e9e-78fb06aaec70",
            "sku_id": "74X0amVozFy40ly3",
            "sku_name": "The educated office item",
            "cost": 57.1,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 8,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "e3c8eb92-915a-43bc-93d5-dcfa68a2cd7b",
            "item_uuid": "31adb57c-a40a-4a99-b3d0-3c6ccd8e8941",
            "item_name": "The cautious knowledge item",
            "sku_uuid": "9060814c-9feb-4a3e-958c-cb26d537cffc",
            "sku_id": "voGDR4gOyYUOgcT7gw",
            "sku_name": "The cautious knowledge item",
            "cost": 6.12,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 6,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "00863921-9254-463a-bba9-969d7820a178",
            "item_uuid": "40769356-76f1-4aa4-8715-252f7ccda8e7",
            "item_name": "The chubby year item",
            "sku_uuid": "7dd19e13-4ae8-49cb-89d6-be0d2add6a9e",
            "sku_id": "5n9brQEbzQK1FY",
            "sku_name": "The chubby year item",
            "cost": 77.58,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 10,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "21d14fe7-7fd4-4880-ba54-2c4bd8e9d3d5",
            "item_uuid": "8fc8bb70-30fb-419a-bd08-8b34197a8065",
            "item_name": "The elated shelf item",
            "sku_uuid": "e37ac193-08f5-41f9-bb88-28b1d6ec249e",
            "sku_id": "KLznQGxkdUAnypK6X0F",
            "sku_name": "The elated shelf item",
            "cost": 24.61,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 5,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "ba8c1057-7700-48cc-82a5-f1e3660d0144",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "d8921492-d8de-43a8-8226-ddcce61014cd",
        "created_date": "2017-10-23T18:29:26.065699Z",
        "notes": "Possimus voluptas in doloremque iusto necessitatibus quo.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Aaron Harrison",
          "business_name": "Jimenez-Jackson",
          "address1": "1729 Reginald Shores\nLake Mercedes, MD 08907-1578",
          "address2": "99930 Mathews Lakes Apt. 086\nBakermouth, GA 75290",
          "city": "Michaelside",
          "state": "Illinois",
          "postal_code": "35564"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "7eb4e06f-e22e-4d2f-84a7-c42680808496",
            "item_uuid": "4911601b-75b2-48d4-ae4d-c61738325335",
            "item_name": "The elated wire item",
            "sku_uuid": "1171a534-9618-4845-8cdb-a3159116d6a8",
            "sku_id": "q3HfYum",
            "sku_name": "The elated wire item",
            "cost": 43.33,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 4,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "135b9cdb-a74a-4019-b3bd-505709b556c9",
            "item_uuid": "89cb0ff0-f524-4bc0-b247-09823cd8c4cc",
            "item_name": "The abnormal cause item",
            "sku_uuid": "e9b0abcf-1d76-40a1-a41e-ed33a637cfbd",
            "sku_id": "QWXs6zdZ",
            "sku_name": "The abnormal cause item",
            "cost": 96.7,
            "supplier_uuid": "0e9dd1c1-1eb5-45dc-9bb0-fe3d53f9da0d",
            "supplier_name": "Sharp, Green and West",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 5,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "baa8f68c-d6ae-474f-9aba-b379b64c870b",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "cbb8defe-19c0-4d18-82f2-1a4b4fe75b83",
        "created_date": "2017-10-23T18:29:26.212242Z",
        "notes": "Quis quod beatae quaerat atque.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Kelly Woods",
          "business_name": "Cox PLC",
          "address1": "19202 Espinoza Stravenue\nNew Sophia, PA 65896",
          "address2": "2564 Rodriguez Lakes Suite 348\nDanielhaven, MS 76702-6283",
          "city": "Brownfort",
          "state": "Wyoming",
          "postal_code": "79461"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "54ccd360-5128-4b81-9a8a-269c6154b208",
            "item_uuid": "a3153e5c-1e86-4209-9c53-293c072cd4a2",
            "item_name": "The capricious sheet item",
            "sku_uuid": "730c61ee-1f2c-4355-ba72-30e82b14d0b4",
            "sku_id": "d5BSKZmoOORSRG",
            "sku_name": "The capricious sheet item",
            "cost": 81.72,
            "supplier_uuid": "62bd2059-2f70-4cd5-9944-ba9969fe5f06",
            "supplier_name": "projectzuul",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 1,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "2eb8fa74-cc72-4793-9d82-9fad2a5d0a4e",
            "item_uuid": "98eb1720-9b1e-49ca-be08-e516e8fb46de",
            "item_name": "The aboard invention item",
            "sku_uuid": "a79a05a8-351f-44b6-94f4-d8a2feebe4db",
            "sku_id": "jfi13jvneLfaiB",
            "sku_name": "The aboard invention item",
            "cost": 94.33,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 6,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "fdde974a-be6c-4429-8f2d-0d5d8e4e471c",
            "item_uuid": "8fc8bb70-30fb-419a-bd08-8b34197a8065",
            "item_name": "The elated shelf item",
            "sku_uuid": "1764f9ed-da2a-4145-9e91-e192340fd5aa",
            "sku_id": "D2LQ8vj",
            "sku_name": "The elated shelf item",
            "cost": 38.79,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 3,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "c3fcaa0e-88f4-4d97-8a70-019418e6c5f6",
            "item_uuid": "97fa8fdf-6b94-409e-a684-841d42605881",
            "item_name": "The changeable soap item",
            "sku_uuid": "995f5edd-7457-4661-9072-e5e9632d8b21",
            "sku_id": "wZtMF91H2tIQ8RU",
            "sku_name": "The changeable soap item",
            "cost": 63.45,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 4,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "6393bcac-0f0f-4b58-899d-1044fb5d32f8",
            "item_uuid": "9bd1c686-0ce1-404c-8055-d52e99e2a987",
            "item_name": "The enraged water item",
            "sku_uuid": "38e58390-e685-4a7c-9ed1-cab9d562d74c",
            "sku_id": "G34Iao",
            "sku_name": "The enraged water item",
            "cost": 17.76,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 6,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "162641ca-a65f-4af0-874f-49f92f03f284",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "12999921-f964-4e68-9d1e-a7d8cc0f1eb2",
        "created_date": "2017-10-23T18:29:26.438023Z",
        "notes": "Inventore vero iste praesentium exercitationem labore in.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Shannon Ortiz",
          "business_name": "Garcia LLC",
          "address1": "33540 Debbie Roads Suite 118\nSouth Stephenberg, WA 51119",
          "address2": "04714 Olsen Crest\nCunninghamport, ID 61122-4628",
          "city": "North Stevenburgh",
          "state": "Indiana",
          "postal_code": "55147"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "cffa1d32-b250-4898-a66d-19640e58761c",
            "item_uuid": "a0acc09b-bbfb-4087-a1ef-8201286980f8",
            "item_name": "The educated office item",
            "sku_uuid": "d6b1f5ce-e98f-41aa-a875-55f9f7a7823c",
            "sku_id": "OLv5wImi44OoiNeYVQG",
            "sku_name": "The educated office item",
            "cost": 71.16,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 3,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "0949e4a5-9ecf-4eff-a85b-f7a0d19ab6bc",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "971757b7-9926-426f-99c6-b68d403f8e3e",
        "created_date": "2017-10-23T18:29:26.550989Z",
        "notes": "Voluptas quos in repellat vitae velit.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Jacob Waters",
          "business_name": "Miller-Jones",
          "address1": "69343 Parsons Estates\nBarrettport, IA 45450-1707",
          "address2": "Unit 3198 Box 5098\nDPO AP 88263-3144",
          "city": "New Kimberly",
          "state": "Arizona",
          "postal_code": "62447"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "3ce88885-fa65-4862-8a5c-9b50d618d0c9",
            "item_uuid": "fffa059b-a4c7-4cac-a288-2a55534c170f",
            "item_name": "The insignificant drawer item",
            "sku_uuid": "a1258298-779a-421c-9f1b-fce82785a5e5",
            "sku_id": "rQwjZr",
            "sku_name": "The insignificant drawer item",
            "cost": 62.66,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 2,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "e8305098-a0cc-4302-b929-9bb5d3f10fd0",
            "item_uuid": "98eb1720-9b1e-49ca-be08-e516e8fb46de",
            "item_name": "The aboard invention item",
            "sku_uuid": "b4490935-bbae-4e6c-80ec-881e6d5a4a34",
            "sku_id": "FOwg6gD",
            "sku_name": "The aboard invention item",
            "cost": 52.24,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 1,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "c6709d1a-312f-4d7f-9d3b-0e3a57c30142",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "3125c626-b6e0-42a5-af05-812a4ac23e87",
        "created_date": "2017-10-23T18:29:26.689657Z",
        "notes": "Magnam laudantium quidem fugiat rerum asperiores perspiciatis.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Jennifer Butler",
          "business_name": "Perry-Wright",
          "address1": "Unit 9813 Box 9351\nDPO AP 07266-5722",
          "address2": "500 Phillip Trafficway Apt. 746\nChrisberg, VT 55460-9870",
          "city": "South George",
          "state": "Louisiana",
          "postal_code": "37162"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "9f7640c2-2ba7-469d-b356-6e86cb514307",
            "item_uuid": "a0acc09b-bbfb-4087-a1ef-8201286980f8",
            "item_name": "The educated office item",
            "sku_uuid": "111a081e-bfe0-4f94-a0ac-fd767999dbd9",
            "sku_id": "9e9Xz4D4yfBqPAaiT",
            "sku_name": "The educated office item",
            "cost": 81.19,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 5,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "3a8d32e8-05ff-4e53-a987-f95e08f18158",
            "item_uuid": "97fa8fdf-6b94-409e-a684-841d42605881",
            "item_name": "The changeable soap item",
            "sku_uuid": "85e575bf-a1c1-4341-80a8-1bdcb9f7aff5",
            "sku_id": "nsjB7Xb",
            "sku_name": "The changeable soap item",
            "cost": 23.89,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 7,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "f8168231-3d0f-48ae-8bbd-4ec3752330bb",
            "item_uuid": "40769356-76f1-4aa4-8715-252f7ccda8e7",
            "item_name": "The chubby year item",
            "sku_uuid": "0849f62b-d7a0-4520-8e23-22f4db3ca605",
            "sku_id": "9XrqDQxxS3z3jcBL3O",
            "sku_name": "The chubby year item",
            "cost": 86.5,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 4,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "f6dfc6b9-ff7a-4498-aa34-efc1432c6c4d",
            "item_uuid": "4911601b-75b2-48d4-ae4d-c61738325335",
            "item_name": "The elated wire item",
            "sku_uuid": "1171a534-9618-4845-8cdb-a3159116d6a8",
            "sku_id": "q3HfYum",
            "sku_name": "The elated wire item",
            "cost": 56.89,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 7,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "a19ee1cd-d9dc-4a78-9fdd-7187181e7270",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "6ebed034-d4f0-4d09-8576-104fb8376caa",
        "created_date": "2017-10-23T18:29:26.873886Z",
        "notes": "Accusantium quidem dicta officiis repellat temporibus eveniet.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "James Pacheco",
          "business_name": "Allen, Spears and Hamilton",
          "address1": "237 Huynh Mount Apt. 162\nWest Cynthialand, MN 13976-7278",
          "address2": "9176 Norman Ramp Apt. 408\nSuareztown, AS 77908-6941",
          "city": "Lake Robertport",
          "state": "New Jersey",
          "postal_code": "39469"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "5b176a39-17c5-4cb9-81f7-66c5f1a970a4",
            "item_uuid": "db6537cc-7e4e-4d98-b7e6-7f9044d9de54",
            "item_name": "The enraged destruction item",
            "sku_uuid": "c386c3e7-5e20-4c27-8356-e74fe92b0226",
            "sku_id": "bg3QAHTREAs",
            "sku_name": "The enraged destruction item",
            "cost": 98.64,
            "supplier_uuid": "0e9dd1c1-1eb5-45dc-9bb0-fe3d53f9da0d",
            "supplier_name": "Sharp, Green and West",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 9,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "3d1ca3ae-40a5-4f3d-8784-151da7a0d02d",
            "item_uuid": "c23c72c4-91d6-492b-9a9b-3738b2e4fd1e",
            "item_name": "The embellished card item",
            "sku_uuid": "e44bbf28-d4dd-4284-9f3c-27df4c1e31df",
            "sku_id": "V9UDm2A9MUvAvT9bT1",
            "sku_name": "The embellished card item",
            "cost": 7.42,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 2,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "98bdf596-1e95-457b-b4b9-82b1bc93a88b",
            "item_uuid": "69672ed3-ba03-4fcb-a34f-c3a4c024c7aa",
            "item_name": "The candid bed item",
            "sku_uuid": "11205f2d-e111-430c-9c8b-69df37e489e9",
            "sku_id": "0vHiHFA9mKw6WOj",
            "sku_name": "The candid bed item",
            "cost": 26.86,
            "supplier_uuid": "1b348539-1f1a-432e-a9c3-63f71e65ad84",
            "supplier_name": "Underwood-Chavez",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 4,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "6affd4bc-795f-42aa-b9b3-3fbe878d5db7",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "68b1a126-23ad-479f-938e-ffc857164809",
        "created_date": "2017-10-23T18:29:27.050181Z",
        "notes": "Asperiores facere praesentium deserunt voluptate explicabo commodi ad inventore.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Dr. Emily Robinson",
          "business_name": "Newman-Perez",
          "address1": "05130 David Road Apt. 460\nLake Jessicahaven, IA 43958-2283",
          "address2": "744 Katherine Plaza\nGeorgeport, TX 37022",
          "city": "South Maria",
          "state": "Nevada",
          "postal_code": "88104"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "54ae44c1-7625-4819-8a90-fe0c0713f255",
            "item_uuid": "c23c72c4-91d6-492b-9a9b-3738b2e4fd1e",
            "item_name": "The embellished card item",
            "sku_uuid": "fe03c2b8-7928-4e48-8e0c-0d58358066ba",
            "sku_id": "ipgOT9iWsOZfg5L",
            "sku_name": "The embellished card item",
            "cost": 13.79,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 2,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "d4628dd8-e458-455f-84f6-30433e6895c6",
            "item_uuid": "31adb57c-a40a-4a99-b3d0-3c6ccd8e8941",
            "item_name": "The cautious knowledge item",
            "sku_uuid": "9060814c-9feb-4a3e-958c-cb26d537cffc",
            "sku_id": "voGDR4gOyYUOgcT7gw",
            "sku_name": "The cautious knowledge item",
            "cost": 46.4,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 6,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "a88345d4-c631-4e44-aed0-c2824a0647e7",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "44fbb3e4-8bc9-4603-bee9-ce758a157637",
        "created_date": "2017-10-23T18:29:27.179614Z",
        "notes": "Vitae dolores perspiciatis corrupti dolore esse.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "David Wright",
          "business_name": "Scott-Garcia",
          "address1": "778 Jacobson Passage\nNew Jaredhaven, OK 87789-9080",
          "address2": "01873 Oliver Turnpike\nRodneybury, ND 98501-4971",
          "city": "West Roymouth",
          "state": "Kansas",
          "postal_code": "19851"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "6d6100fe-6fd8-4f15-b365-98cb228cf08b",
            "item_uuid": "8e1898de-4bee-46ef-b242-16ddfacfd350",
            "item_name": "The innocent competition item",
            "sku_uuid": "76302a53-d895-4711-b527-f13794690787",
            "sku_id": "cZ0iHJYxMCqzf",
            "sku_name": "The innocent competition item",
            "cost": 13.29,
            "supplier_uuid": "62bd2059-2f70-4cd5-9944-ba9969fe5f06",
            "supplier_name": "projectzuul",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 1,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "64cf3679-ff49-4f7b-9817-ea3acc5651fe",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "6f76c905-a001-4f02-a554-0f180f9437ec",
        "created_date": "2017-10-23T18:29:27.289526Z",
        "notes": "Repudiandae officia sed nihil et.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Miguel Stevens",
          "business_name": "Soto, Flores and Chaney",
          "address1": "18572 Sullivan Ports Apt. 661\nReyesland, NV 37074",
          "address2": "90190 Michele Radial\nJasonborough, MD 26692",
          "city": "Port Laura",
          "state": "Hawaii",
          "postal_code": "43705"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "af547860-6882-42a4-a54f-c99f9985403d",
            "item_uuid": "31adb57c-a40a-4a99-b3d0-3c6ccd8e8941",
            "item_name": "The cautious knowledge item",
            "sku_uuid": "697d3dda-c086-4190-a8c5-3527fc52afc5",
            "sku_id": "kfEoZWI",
            "sku_name": "The cautious knowledge item",
            "cost": 87.97,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 8,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "c301d9be-a117-49b0-9c63-7e9ed3de6188",
            "item_uuid": "8fc8bb70-30fb-419a-bd08-8b34197a8065",
            "item_name": "The elated shelf item",
            "sku_uuid": "e37ac193-08f5-41f9-bb88-28b1d6ec249e",
            "sku_id": "KLznQGxkdUAnypK6X0F",
            "sku_name": "The elated shelf item",
            "cost": 36.45,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 9,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "350c3ebc-bb09-4b15-b3d1-1698cc8eddfa",
            "item_uuid": "db6537cc-7e4e-4d98-b7e6-7f9044d9de54",
            "item_name": "The enraged destruction item",
            "sku_uuid": "d00a6590-3943-4683-936a-c990e874e823",
            "sku_id": "39hq09VpQ12Dw",
            "sku_name": "The enraged destruction item",
            "cost": 88.36,
            "supplier_uuid": "0e9dd1c1-1eb5-45dc-9bb0-fe3d53f9da0d",
            "supplier_name": "Sharp, Green and West",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 2,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "c287f1a1-bbde-4c10-931c-5861bd2fd4f4",
            "item_uuid": "31adb57c-a40a-4a99-b3d0-3c6ccd8e8941",
            "item_name": "The cautious knowledge item",
            "sku_uuid": "9060814c-9feb-4a3e-958c-cb26d537cffc",
            "sku_id": "voGDR4gOyYUOgcT7gw",
            "sku_name": "The cautious knowledge item",
            "cost": 22.4,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 5,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "2d9b491d-2db7-458d-8e47-03351b809609",
            "item_uuid": "31adb57c-a40a-4a99-b3d0-3c6ccd8e8941",
            "item_name": "The cautious knowledge item",
            "sku_uuid": "9060814c-9feb-4a3e-958c-cb26d537cffc",
            "sku_id": "voGDR4gOyYUOgcT7gw",
            "sku_name": "The cautious knowledge item",
            "cost": 80.7,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 10,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "82940fcc-d3c9-479d-8a5c-c3dbd3ca1e44",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "d4f88861-16bb-45ee-b846-93c75b37df4e",
        "created_date": "2017-10-23T18:29:27.486641Z",
        "notes": "Aspernatur vitae dolor quidem aperiam laudantium quas corporis.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Allen Spencer",
          "business_name": "Lucas, Watts and Rice",
          "address1": "48410 Soto Knoll\nDaughertyfort, PW 17762",
          "address2": "378 Barton Manors\nSmithland, SC 82897-3610",
          "city": "Michaelstad",
          "state": "Rhode Island",
          "postal_code": "27947"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "0bc727b3-bdfd-4ab5-912a-75632f4a8a52",
            "item_uuid": "a0acc09b-bbfb-4087-a1ef-8201286980f8",
            "item_name": "The educated office item",
            "sku_uuid": "63ca88d9-91e2-4bd8-8e9e-78fb06aaec70",
            "sku_id": "74X0amVozFy40ly3",
            "sku_name": "The educated office item",
            "cost": 1.8,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 6,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "8a0372cc-3c40-4b5c-a221-66399d1a7ca9",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "af0c83b8-11b0-4216-9502-f39a356f49fd",
        "created_date": "2017-10-23T18:29:27.595987Z",
        "notes": "Laudantium nihil delectus consectetur debitis.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Lindsay Reeves",
          "business_name": "Thompson-Parks",
          "address1": "74638 Tanya Loaf Apt. 264\nCynthiamouth, CO 12888-5073",
          "address2": "78351 Austin Neck Suite 774\nNorth John, MT 28674-3530",
          "city": "Torresborough",
          "state": "Vermont",
          "postal_code": "77771"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "39d6194b-9e67-4987-a6f3-d849b1dc021e",
            "item_uuid": "781689a7-79a2-4bda-8929-cee441336c8c",
            "item_name": "The accomplished stretch item",
            "sku_uuid": "538de9db-4a88-48b2-8b29-95d806bf3e06",
            "sku_id": "UUYJ6y1hIo",
            "sku_name": "The accomplished stretch item",
            "cost": 63.85,
            "supplier_uuid": "62bd2059-2f70-4cd5-9944-ba9969fe5f06",
            "supplier_name": "projectzuul",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 5,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "5f70ac6b-c1a0-4217-becc-c1dc6bf6719b",
            "item_uuid": "40769356-76f1-4aa4-8715-252f7ccda8e7",
            "item_name": "The chubby year item",
            "sku_uuid": "0849f62b-d7a0-4520-8e23-22f4db3ca605",
            "sku_id": "9XrqDQxxS3z3jcBL3O",
            "sku_name": "The chubby year item",
            "cost": 45.84,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 5,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "db34c642-f31b-4c7b-a05a-076ac7348820",
            "item_uuid": "40769356-76f1-4aa4-8715-252f7ccda8e7",
            "item_name": "The chubby year item",
            "sku_uuid": "7dd19e13-4ae8-49cb-89d6-be0d2add6a9e",
            "sku_id": "5n9brQEbzQK1FY",
            "sku_name": "The chubby year item",
            "cost": 87.83,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 6,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "d94fe40f-9b13-42cc-bb42-286f86d062fa",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "5b247f09-ee4b-4998-8a18-6288af4c17f6",
        "created_date": "2017-10-23T18:29:27.776123Z",
        "notes": "Labore nemo quia laudantium eaque magnam.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Joseph Merritt",
          "business_name": "Cisneros-Richardson",
          "address1": "39063 Zachary Pike Apt. 242\nSouth Alec, KY 05723-2241",
          "address2": "572 Steven Islands\nRachelland, VT 34082",
          "city": "North Kenneth",
          "state": "Nevada",
          "postal_code": "04624"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "c0d540d2-8165-47bc-a84f-ebeaeb7bacb3",
            "item_uuid": "a3153e5c-1e86-4209-9c53-293c072cd4a2",
            "item_name": "The capricious sheet item",
            "sku_uuid": "06bcecbc-8e2e-4cae-9b9b-294bcf74836e",
            "sku_id": "OIzMTQdpev4N1n1MH1t",
            "sku_name": "The capricious sheet item",
            "cost": 15.48,
            "supplier_uuid": "62bd2059-2f70-4cd5-9944-ba9969fe5f06",
            "supplier_name": "projectzuul",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 1,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "d3442134-5fab-4282-b3b0-aed542e4c6de",
            "item_uuid": "a0acc09b-bbfb-4087-a1ef-8201286980f8",
            "item_name": "The educated office item",
            "sku_uuid": "d6b1f5ce-e98f-41aa-a875-55f9f7a7823c",
            "sku_id": "OLv5wImi44OoiNeYVQG",
            "sku_name": "The educated office item",
            "cost": 8.72,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 6,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "9cda371f-6049-48d9-8e52-0533d72530ee",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "16324252-1bd2-45d7-8249-d2f3e6ebfda9",
        "created_date": "2017-10-23T18:29:27.908730Z",
        "notes": "Adipisci commodi voluptatum quis quos.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Jaime Smith",
          "business_name": "Pierce, Mcmahon and Molina",
          "address1": "9907 Jason Ville Apt. 298\nPort Lisafurt, AZ 14484-1461",
          "address2": "57622 Nguyen Spring Suite 602\nNathanfort, IA 35009-6994",
          "city": "Pamelaport",
          "state": "California",
          "postal_code": "38269"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "9a049ec3-27a5-4e9e-a875-c9c589a21c01",
            "item_uuid": "97fa8fdf-6b94-409e-a684-841d42605881",
            "item_name": "The changeable soap item",
            "sku_uuid": "99b95146-c484-425a-81e0-378d2fea4b61",
            "sku_id": "mRVWcwTZKYjrOpH9iQ5",
            "sku_name": "The changeable soap item",
            "cost": 49.79,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 6,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "6f02a033-6a52-4c3f-81af-84b6c5e2958c",
            "item_uuid": "0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017",
            "item_name": "The capital arch item",
            "sku_uuid": "0cf678be-7dd1-47e3-852c-e80942d5566b",
            "sku_id": "UfvfG2",
            "sku_name": "The capital arch item",
            "cost": 81.47,
            "supplier_uuid": "1b348539-1f1a-432e-a9c3-63f71e65ad84",
            "supplier_name": "Underwood-Chavez",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 3,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "478c27a1-75e7-46fc-a39a-33e4399f476b",
            "item_uuid": "866091fa-a28f-4f7b-ac32-4f6c952204ab",
            "item_name": "The canine recess item",
            "sku_uuid": "033c10bf-de9b-4493-a804-ce306a85bee7",
            "sku_id": "Db6HXa72AfRHfkcUC",
            "sku_name": "The canine recess item",
            "cost": 40.83,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 5,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "4790f16d-320c-4947-99e2-b797edb8721a",
            "item_uuid": "0134a3b5-be78-4a2a-a9b7-e2a5ecbcf017",
            "item_name": "The capital arch item",
            "sku_uuid": "0cf678be-7dd1-47e3-852c-e80942d5566b",
            "sku_id": "UfvfG2",
            "sku_name": "The capital arch item",
            "cost": 6.7,
            "supplier_uuid": "1b348539-1f1a-432e-a9c3-63f71e65ad84",
            "supplier_name": "Underwood-Chavez",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 3,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "9d34449d-d86e-4016-8057-5dcfbca5a95d",
            "item_uuid": "31adb57c-a40a-4a99-b3d0-3c6ccd8e8941",
            "item_name": "The cautious knowledge item",
            "sku_uuid": "1ba7a1e7-0eb3-46ae-875f-67d65caa94fa",
            "sku_id": "ok8AM531hs",
            "sku_name": "The cautious knowledge item",
            "cost": 97.8,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 8,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "1e1f0ea4-2d71-406a-a9a1-33d15cf5e09c",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "41d26890-489c-4884-9315-b40671f9ff02",
        "created_date": "2017-10-23T18:29:28.304429Z",
        "notes": "Aperiam nisi delectus eum reiciendis quae.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Brenda Barry",
          "business_name": "Snyder-Cross",
          "address1": "891 Omar Spur Apt. 560\nNew Williammouth, VI 09384",
          "address2": "USNS Turner\nFPO AP 76321-5036",
          "city": "Johnton",
          "state": "Montana",
          "postal_code": "41336"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "8887d4f4-85f1-47c6-b424-05493ae910f1",
            "item_uuid": "97fa8fdf-6b94-409e-a684-841d42605881",
            "item_name": "The changeable soap item",
            "sku_uuid": "995f5edd-7457-4661-9072-e5e9632d8b21",
            "sku_id": "wZtMF91H2tIQ8RU",
            "sku_name": "The changeable soap item",
            "cost": 13.4,
            "supplier_uuid": "48e81e45-4462-4c9b-b0d6-9226fdede7a6",
            "supplier_name": "Flynn Ltd",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 10,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "f9b93563-b360-43d6-ae30-cbf1361d283e",
            "item_uuid": "358d6043-220f-4107-93b7-1c22151dd5f0",
            "item_name": "The infamous blood item",
            "sku_uuid": "283d8682-0124-4bc4-917b-6c49e66bb2b0",
            "sku_id": "PKvjWdRBlDFXIaYWFcE",
            "sku_name": "The infamous blood item",
            "cost": 44.6,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 4,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "86b3d5d1-e0a0-4bc4-85f0-39b3c6662aa8",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "89169f5f-d92f-4d91-a113-62965ee0e13b",
        "created_date": "2017-10-23T18:29:28.549509Z",
        "notes": "Pariatur magnam laudantium atque.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Mark Davidson",
          "business_name": "Wright-Castillo",
          "address1": "16978 Blackburn Fall Suite 744\nGarciafurt, MT 68290",
          "address2": "01124 Stephen Fort Apt. 996\nLake Carla, CO 48696-5005",
          "city": "Hendersonhaven",
          "state": "California",
          "postal_code": "53688"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "0aba4767-4caf-4108-84b6-90365bb32eb9",
            "item_uuid": "8e1898de-4bee-46ef-b242-16ddfacfd350",
            "item_name": "The innocent competition item",
            "sku_uuid": "260a181a-331e-4e4f-9a57-510048a5d3f2",
            "sku_id": "bpSH45MO",
            "sku_name": "The innocent competition item",
            "cost": 58.23,
            "supplier_uuid": "62bd2059-2f70-4cd5-9944-ba9969fe5f06",
            "supplier_name": "projectzuul",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 9,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "dfe8a938-2b9c-4253-b100-8a8d5a54312a",
            "item_uuid": "759db03f-0e79-4037-9650-411251b5aa12",
            "item_name": "The cheery care item",
            "sku_uuid": "66f8b469-f702-4e4f-89ec-b7131a5225f1",
            "sku_id": "5Z0CurC5",
            "sku_name": "The cheery care item",
            "cost": 56.97,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 8,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "d1c34c88-e3db-48ac-bbb3-a0f7bce97a77",
            "item_uuid": "db6537cc-7e4e-4d98-b7e6-7f9044d9de54",
            "item_name": "The enraged destruction item",
            "sku_uuid": "ec26763f-5395-47b7-b7bb-f0ce03058e1d",
            "sku_id": "USaoDXIiLNHOgNy",
            "sku_name": "The enraged destruction item",
            "cost": 87.72,
            "supplier_uuid": "0e9dd1c1-1eb5-45dc-9bb0-fe3d53f9da0d",
            "supplier_name": "Sharp, Green and West",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 3,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "3c56aba9-6879-475c-a1d1-f2b55cd55509",
            "item_uuid": "c23c72c4-91d6-492b-9a9b-3738b2e4fd1e",
            "item_name": "The embellished card item",
            "sku_uuid": "80588a81-fdc5-41bf-85ae-431d923f0d8d",
            "sku_id": "QyTsBbEK8Y5fYzee",
            "sku_name": "The embellished card item",
            "cost": 16.8,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 4,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "038c268d-4c22-49dc-ab28-2ef2ce365926",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "a3d1f12b-332b-4244-91e0-e2d64969769c",
        "created_date": "2017-10-23T18:29:28.744834Z",
        "notes": "Fugit maiores suscipit illo non ex a.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Philip Thompson",
          "business_name": "Martinez, Conway and Parker",
          "address1": "1472 Kristine Park\nPort Gabrielashire, HI 21759-4745",
          "address2": "957 Mercado Walks Apt. 959\nChristopherstad, SD 49427-2660",
          "city": "South Lisachester",
          "state": "Minnesota",
          "postal_code": "06845"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "d094313e-4370-4c18-9c17-28016d81ca05",
            "item_uuid": "358d6043-220f-4107-93b7-1c22151dd5f0",
            "item_name": "The infamous blood item",
            "sku_uuid": "ddb24660-4ba3-47b5-95f3-99053946ef1f",
            "sku_id": "woW066XbzFfA",
            "sku_name": "The infamous blood item",
            "cost": 98.59,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 8,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "e01069ac-e718-4025-91b7-4d79954c50d3",
            "item_uuid": "69672ed3-ba03-4fcb-a34f-c3a4c024c7aa",
            "item_name": "The candid bed item",
            "sku_uuid": "11205f2d-e111-430c-9c8b-69df37e489e9",
            "sku_id": "0vHiHFA9mKw6WOj",
            "sku_name": "The candid bed item",
            "cost": 32.92,
            "supplier_uuid": "1b348539-1f1a-432e-a9c3-63f71e65ad84",
            "supplier_name": "Underwood-Chavez",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 7,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "c7fa14fa-c6ba-4611-ae54-2c119760552c",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "037fbedd-050b-4140-a2ea-3347bd6f5822",
        "created_date": "2017-10-23T18:29:28.877659Z",
        "notes": "Quaerat quibusdam voluptatum dolorum tenetur voluptate numquam quis.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Samantha Brown",
          "business_name": "Patterson LLC",
          "address1": "73824 Nancy Court\nSamuelville, MH 01433-4300",
          "address2": "7607 Ross Mills Apt. 801\nEast Heiditon, MS 91323",
          "city": "Crystalchester",
          "state": "Nebraska",
          "postal_code": "87668"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "b5b698fd-068e-47e3-a6c2-35d0c6278b24",
            "item_uuid": "40769356-76f1-4aa4-8715-252f7ccda8e7",
            "item_name": "The chubby year item",
            "sku_uuid": "16e1122a-793e-4511-8875-39e2d846cedf",
            "sku_id": "EaDRBL1xHPKFy8Cztt",
            "sku_name": "The chubby year item",
            "cost": 14.22,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 2,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      },
      {
        "uuid": "a274fb88-ac87-4fb7-b2ab-be64edb7e729",
        "status": "New",
        "is_allocated": false,
        "purchase_order_id": "497c3607-f75b-4ada-aebd-2eab1a36596a",
        "created_date": "2017-10-23T18:29:28.984911Z",
        "notes": "Hic itaque sapiente nostrum debitis quo excepturi inventore itaque.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "projectthanos",
          "uuid": "e7409ece-e923-4aa8-a41b-4aacb9e475be",
          "user": {
            "name": " ",
            "email": "dchadwick@projectthanos.com"
          }
        },
        "address": {
          "name": "Christopher Garcia",
          "business_name": "Rogers, Carter and Howard",
          "address1": "6130 Caldwell Union\nWilliamsview, WI 34000-9545",
          "address2": "86303 Victoria Oval Suite 287\nWest Janet, NC 50642",
          "city": "Hannaton",
          "state": "Oklahoma",
          "postal_code": "41772"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "611e836c-9538-4001-b067-4e96088f164c",
            "item_uuid": "a3153e5c-1e86-4209-9c53-293c072cd4a2",
            "item_name": "The capricious sheet item",
            "sku_uuid": "2925cf50-5382-4c12-b54c-0017411e20df",
            "sku_id": "cGBATYRe6hPf3VY",
            "sku_name": "The capricious sheet item",
            "cost": 14.94,
            "supplier_uuid": "62bd2059-2f70-4cd5-9944-ba9969fe5f06",
            "supplier_name": "projectzuul",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 5,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "dfad5515-ad20-4940-93be-a653139bf656",
            "item_uuid": "8fc8bb70-30fb-419a-bd08-8b34197a8065",
            "item_name": "The elated shelf item",
            "sku_uuid": "1764f9ed-da2a-4145-9e91-e192340fd5aa",
            "sku_id": "D2LQ8vj",
            "sku_name": "The elated shelf item",
            "cost": 96.23,
            "supplier_uuid": "2ed7b9ed-671e-4699-aaba-c96c0fd43c0a",
            "supplier_name": "Garcia-Arias",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 9,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "8d6aa41c-b8d2-42b2-b409-bf8325633686",
            "item_uuid": "358d6043-220f-4107-93b7-1c22151dd5f0",
            "item_name": "The infamous blood item",
            "sku_uuid": "c3786845-3f06-4a10-a6cd-ff23461ab11f",
            "sku_id": "yl3t2Lij7XJfAnsB",
            "sku_name": "The infamous blood item",
            "cost": 3.45,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 5,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "fab803a3-17a5-4061-b4d7-3ee2d23d6cc8",
            "item_uuid": "8e1898de-4bee-46ef-b242-16ddfacfd350",
            "item_name": "The innocent competition item",
            "sku_uuid": "4fc3e083-0828-4842-b647-13bcf7564dac",
            "sku_id": "s1lqyjs0KuRTg",
            "sku_name": "The innocent competition item",
            "cost": 0.29,
            "supplier_uuid": "62bd2059-2f70-4cd5-9944-ba9969fe5f06",
            "supplier_name": "projectzuul",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 4,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "6c081e83-bec5-4fa9-a3f7-e582c503ab6b",
            "item_uuid": "40769356-76f1-4aa4-8715-252f7ccda8e7",
            "item_name": "The chubby year item",
            "sku_uuid": "7dd19e13-4ae8-49cb-89d6-be0d2add6a9e",
            "sku_id": "5n9brQEbzQK1FY",
            "sku_name": "The chubby year item",
            "cost": 64.48,
            "supplier_uuid": "4b72cfbc-5123-4152-a7ed-3da5d0ce8bad",
            "supplier_name": "Brooks-Jones",
            "tracking_numbers": [],
            "allocation": {
              "quantity_ordered": 2,
              "quantity_allocated": 0,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          }
        ]
      }
    ]
  }
  ~~~
  {: title="Response" }

---
Get the complete List of Orders for your organization. This list contains all of your orders: completed, incomplete, processing, etc. Your username and password are optional as you can send your authorization token to receive this information.

URL Endpoint: /api/orders/

### Request Parameters:

#### Optional:

start
: (number) The Start is the number of which "Order" you would like to start. If no other filters are used, the default order, which is date created, is used. The default Start value is 0. If this filter is not included in your request, the default value is used.

limit
: (number) The Limit is the element number of "Order" in your Orders List where you would like your results to end. If you have 10 orders and you limit at 8 and start at 4, only orders 4, 5, 6, 7, and 8 are included in the results.

sort
: (object) The Sort object contains a Key to sort on and a Direction (dir) to sort in

status
: (string) The Status of the Orders you would like to see returned

start_date
: (string) The Start Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

end_date
: (string) The End Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

##### Sort Object:

key
: (string) The Key is the attribute on which you'd like to sort. Possible values include date, status, and sku_id.

dir
: (string) The Direction is ascending or descending entered as "asc" or "des"

### Response Parameters:

total_results
: (number) The Total Results are the total order count per your oganization

orders
: (list) The list of orders per your organization

#### Order Object:

uuid
: (string) The Universal Unique Identifier for the Order

status
: (string) The current Status of the Order

is_allocated
: (boolean) Is the order Allocated by the Supplier as of the moment you get the response. Generally, this is false initially as the supplier(s) providing the SKU(s) must allocate for each Order.

purchase_order_id
: (string) The Purchase Order (PO) Identifier for this order. This is the one you provided in the request parameters. It is the Identifer that your organization uses to identify the Order.

created_date
: (string) The Date when the order was created. It will always be the same day as when you send in the request to Create the Order.

notes
: (string) The notes you provided from your request to create the Order.

fees
: (object) The Fees object contains the estimated shipping cost, drop ship fee, and order fee

retailer
: (object) The Retailer object contains an organization name, organization uuid, and a user object

address
: (object) The Address object containing name, business name, address line 1, address line 2, city, state, postal code

requested_shipping
: (object) The Requested Shipping object contains the shipping carrier and shipping method from the request to create the Order.

line_items
: (list) The Line Items list contains line items with their uuid, item uuid, item name, sku uuid, sku id, sku name, cost, supplier uuid, supplier name, tracking numbers list, and allocation object.

#### Fees Object:

estimated_shipping_cost
: (number) The Estimated Shipping Cost for the Order

drop_ship_fee
: (number) The Drop Ship Fee for the Order as charged by the Supplier

order_fee
: (number) The Order Fee charged for processing the order through our platform

#### Retailer Object:

name
: (string) The Organization Name within your Retailer account

uuid
: (string) The Universal Unique Identifier for your Organization

user
: (object) The User object contains your name and email address; the name and email address of the user who submitted the Create Order API call.

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
: (number) The Zip Code / Postal Code associated with the Address

#### Requested Shipping Object:

shipping_carrier
: (string) The Shipping Carrier to deliver the order

shipping_method
: (string) The Shipping Method used by the Shipping Carrier to deliver the order

#### Line Item Object:

uuid
: (string) Universal Unique Identifier for the Line Item

item_uuid
: (string) Universal Unique Identifier for the Item

item_name
: (string) The Item Name

sku_uuid
: (string) The Univeral Unique Identifier for the SKU

sku_id
: (string) The SKU as provided by the Supplier

sku_name
: (string) The SKU Name

cost
: (number) The Cost of the SKU

supplier_uuid
: (string) The Universal Unique Identifier for the Supplier

supplier_name
: (string) The Supplier Name

tracking_numbers
: (list) The Tracking Numbers list provides a Tracking Number or list of multiple Tracking Numbers for this particular SKU.

allocation
: (object) The Allocation object contains quantity ordered, quantity allocated, quantity backordered, quantity rejected, and backorder date.

#### Allocation Object:

quantity_ordered
: (number) The Quantity Ordered of the SKU

quantity_allocated
: (number) The Quantity Allocated by the Supplier for this Order

quantity_backordered
: (number) The Quantity Backordered is the quantity of the order that cannot be shipped because it is currently in a "backordered" state. If you allow the supplier to fulfill the order, this number is supposed to decrease to 0 as they get the item in-stock in their warehouse(s). When a Supplier gets a Backorder Date, they add it to the field labeled "backorder_date".

quantity_rejected
: (number) The Quantity Rejected by the Supplier is the Quantity that they simply cannot fulfill. Reasons may vary, such as state or federal law, customs, or being out-of-stock on an already discontinued product line.

backorder_date
: (string) The Date that the Backordered SKU will be available for shipment. This date should be used as a tentative schedule which may help determine if waiting for the order is appropriate. Should this date be unacceptable, you may cancel the order with the "Cancel Order" API call.

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl -X "POST" "https://stable.projectthanos.com/api/orders/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "limit": 25,
  "status": "New",
  "end_date": "2018-08-03T06:00:00.000Z",
  "sort": {
    "key": "uuid",
    "dir": "des"
  },
  "start_date": "2017-07-31T06:00:00.000Z",
  "start": 0
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://stable.projectthanos.com/api/orders/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8' \
    limit:=25 \
    status="New" \
    end_date="2018-08-03T06:00:00.000Z" \
    sort:="{
  \"key\": \"uuid\",
  \"dir\": \"des\"
}" \
    start_date="2017-07-31T06:00:00.000Z" \
    start:=0

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Order List
    # POST https://stable.projectthanos.com/api/orders/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/orders/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    limit:=25 \
    status="New" \
    end_date="2018-08-03T06:00:00.000Z" \
    sort:="{
  \"key\": \"uuid\",
  \"dir\": \"des\"
}" \
    start_date="2017-07-31T06:00:00.000Z" \
    start:=0)
        )
        print('Response HTTP Status Code: {status_code}'.format(
            status_code=response.status_code))
        print('Response HTTP Response Body: {content}'.format(
            content=response.content))
    except requests.exceptions.RequestException:
        print('HTTP Request failed')

~~~
{: title="Python (requests)" }

~~~ javascript
// request Get Order List
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/orders/',
        method: 'POST',
        headers: {"Authorization":"Token a0f17278bed479ee719ea890b8caf0329e1f3e5b","Content-Type":"application/json; charset=utf-8"}
    };
    httpOptions.headers['User-Agent'] = 'node ' + process.version;


    const request = httpTransport.request(httpOptions, (res) => {
        let responseBufs = [];
        let responseStr = '';

        res.on('data', (chunk) => {
            if (Buffer.isBuffer(chunk)) {
                responseBufs.push(chunk);
            }
            else {
                responseStr = responseStr + chunk;
            }
        }).on('end', () => {
            responseStr = responseBufs.length > 0 ?
                Buffer.concat(responseBufs).toString(responseEncoding) : responseStr;

            callback(null, res.statusCode, res.headers, responseStr);
        });

    })
    .setTimeout(0)
    .on('error', (error) => {
        callback(error);
    });
    request.write("{\"start\":0,\"limit\":25,\"sort\":{\"key\":\"uuid\",\"dir\":\"des\"},\"status\":\"New\",\"start_date\":\"2017-07-31T06:00:00.000Z\",\"end_date\":\"2018-08-03T06:00:00.000Z\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
