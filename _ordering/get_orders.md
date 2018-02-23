---
title: /orders/
name: Get Orders
position: 0
method: post
description: Get the Order List for your organization
right_code: |
  ~~~ json
  {
    "start": 0,
    "limit": 25,
    "line_item_statuses": [
      "unallocated"
    ],
    "line_item_status_conjunction": "or",
    "start_date": "2017-07-31T06:00:00.000Z",
    "end_date": "2018-08-03T06:00:00.000Z",
    "term": "",
    "org_uuids": []
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "total_results": 101,
    "orders": [
      {
        "uuid": "10307ca4-c702-4a44-abb3-3828e67bdbb9",
        "is_allocated": false,
        "purchase_order_id": "4225a169-c912-438c-be13-fcfbf9c6ba5e",
        "created_date": "2018-02-13T23:50:45.118818Z",
        "notes": "Accusamus voluptatem beatae quibusdam quia ex consequatur.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Mr. Daniel Morales",
          "business_name": "Gonzalez, Fisher and Richmond",
          "address1": "234 Sandra Cove Suite 835\nJosephfort, ID 04759",
          "address2": "851 Gutierrez Fork\nNorth Marystad, MI 54955",
          "city": "Port Ryanstad",
          "state": "Missouri",
          "postal_code": "28806",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "0f022062-6ec8-4beb-97cf-02fe3d2c5820",
            "status": "Unallocated",
            "item_uuid": "041a4cf0-a4a6-46eb-a61c-a87b28995557",
            "item_name": "Frogg Toggs Pro Lite Rain Suit Royal Blue - X/XXL",
            "sku_uuid": "adc3c7f0-8811-4c56-a968-2d88c9dcfd92",
            "sku_id": "1002664",
            "sku_name": "Frogg Toggs Pro Lite Rain Suit Royal Blue - X/XXL",
            "cost": 39.6,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "7b90f9d5-6497-48e6-8b70-61f669f8e8d4",
            "status": "Unallocated",
            "item_uuid": "f45deb3e-2f98-41b9-85d6-d50b8f9557f2",
            "item_name": "Spyderco Endura4 Lightweight Black FRN Comboedge",
            "sku_uuid": "4b89350e-27f7-4d55-b643-b8f1d3b64f18",
            "sku_id": "000951",
            "sku_name": "Spyderco Endura4 Lightweight Black FRN Comboedge",
            "cost": 51.38,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "980b9534-42b1-4c05-8bf1-ff8b5c966d63",
            "status": "Unallocated",
            "item_uuid": "51041ea6-8946-42f7-96a8-ac9ed9a17119",
            "item_name": "Genesis Original Righthand Bow Green",
            "sku_uuid": "e5cc3d99-19ed-4d6e-bef9-1aef50f33c4a",
            "sku_id": "000192",
            "sku_name": "Genesis Original Righthand Bow Green",
            "cost": 68.46,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "0e29ee59-cc01-4698-b462-84f3b7f43f34",
            "status": "Unallocated",
            "item_uuid": "88d1cee7-9ee3-447e-82cf-0a9591bd1c86",
            "item_name": "Women’s Motivation Tech Bra",
            "sku_uuid": "4e85d942-b411-495a-ad09-3cac30f86244",
            "sku_id": "NF0A2VARFTH-S",
            "sku_name": "Women’s Motivation Tech Bra",
            "cost": 37.21,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "7c37c3d3-d90c-4f86-8d7c-2ba43ce882dd",
            "status": "Unallocated",
            "item_uuid": "2ba73e2a-bd96-47c9-9317-045101e35674",
            "item_name": "Women’s Freedom Insulated Pant",
            "sku_uuid": "6effebfa-ee19-47f3-8634-f3a3b40967a6",
            "sku_id": "NF0A3337FN4-XL-SHT",
            "sku_name": "Women’s Freedom Insulated Pant",
            "cost": 54.38,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "99098c96-1c29-4628-9621-104e4efbe530",
        "is_allocated": false,
        "purchase_order_id": "884009bf-7f42-4521-9649-1dc17d626162",
        "created_date": "2018-02-13T23:50:45.639273Z",
        "notes": "Dolorem id quibusdam fuga cupiditate.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Robert Madden",
          "business_name": "Abbott and Sons",
          "address1": "7441 Patel Stream Apt. 798\nScottton, NM 96076-7314",
          "address2": "118 Benson Green Suite 921\nSimsbury, FL 61826-8547",
          "city": "Vargasside",
          "state": "South Dakota",
          "postal_code": "41902",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "ae0f731c-450f-4089-b774-4fbcb467fb78",
            "status": "Unallocated",
            "item_uuid": "26dc6fde-3df9-4890-8f91-7cb6d9a6a0a5",
            "item_name": "CAA ADJ CHEEK PIECE FOR(CBS)STK BLK",
            "sku_uuid": "2aefc078-a949-48fe-b1ac-711a092aaa74",
            "sku_id": "CAAACP",
            "sku_name": "CAA ADJ CHEEK PIECE FOR(CBS)STK BLK",
            "cost": 81.64,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "e58cb1b2-0180-4fd1-af91-3e0188c61d1e",
            "status": "Unallocated",
            "item_uuid": "04f0a708-3b07-4b1d-bd06-8d8fd157b9e0",
            "item_name": "Women’s Campshire Pullover Hoodie",
            "sku_uuid": "cf5375a1-7189-496b-865c-0c50e34fe3dd",
            "sku_id": "NF0A39MRRKT-M",
            "sku_name": "Women’s Campshire Pullover Hoodie",
            "cost": 73.43,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "9fe749f8-65cd-43ed-8868-bb9e06946648",
            "status": "Unallocated",
            "item_uuid": "0c56f25b-055e-4888-8b62-f23f434a5067",
            "item_name": "Women’s 3L Triclimate&#174; Jacket",
            "sku_uuid": "5060c6d2-c239-433e-a6f4-8033bf14278c",
            "sku_id": "NF0A3373EKJ-M",
            "sku_name": "Women’s 3L Triclimate&#174; Jacket",
            "cost": 94.37,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "19848dea-946e-477c-89b6-8456dfaed48c",
            "status": "Unallocated",
            "item_uuid": "aa91eeef-a2f6-4fce-aa87-126711bea801",
            "item_name": "Boys’ ThermoBall&#8482; Full Zip Jacket",
            "sku_uuid": "f827dad1-b381-4a29-a484-9447deab4687",
            "sku_id": "NF0A34QHWYF-XS",
            "sku_name": "Boys’ ThermoBall&#8482; Full Zip Jacket",
            "cost": 1.42,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "3ae1f5ea-4934-40c3-8cb7-dd09e81907d2",
            "status": "Unallocated",
            "item_uuid": "8cb80256-f557-4529-bb45-9a751c808381",
            "item_name": "Men’s Hedgehog Fastpack GTX&#174;",
            "sku_uuid": "9b165fd9-0db3-4f94-afbf-1b8e5cf11629",
            "sku_id": "NF00CDF8YLF-125",
            "sku_name": "Men’s Hedgehog Fastpack GTX&#174;",
            "cost": 68.69,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "492d97af-b839-4d8a-98a5-855f9c6549e0",
        "is_allocated": false,
        "purchase_order_id": "6921c3e6-17f2-4f36-957c-56afb8a888a1",
        "created_date": "2018-02-13T23:50:46.182221Z",
        "notes": "Molestias minus ex rerum velit debitis.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Crystal Murphy",
          "business_name": "Fletcher and Sons",
          "address1": "28346 Wilson Roads Apt. 824\nNorth Cynthia, ID 28454",
          "address2": "712 Anna Fall Apt. 108\nRiverashire, IA 23045",
          "city": "East Robert",
          "state": "Hawaii",
          "postal_code": "81812",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "e227e638-b46b-4171-8cc1-21db2efe7b7b",
            "status": "Unallocated",
            "item_uuid": "bb350f6e-085d-44ad-9947-5009f4151e37",
            "item_name": "ALLEN PISTOL RUG 6\" ASS'T COLORS",
            "sku_uuid": "81f4704b-d2be-4065-bb4b-9fba3a9f7c33",
            "sku_id": "ALN726",
            "sku_name": "ALLEN PISTOL RUG 6\" ASS'T COLORS",
            "cost": 83.6,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "cc5b01fa-ede5-441b-9b23-7bbecff24705",
            "status": "Unallocated",
            "item_uuid": "1c7218fe-0970-44dc-bd8a-6d3bc9c206a2",
            "item_name": "BH HIP HLSTR SZ 2 RH BLK",
            "sku_uuid": "ed509d98-ba80-4170-995a-f8969b4053e8",
            "sku_id": "BH73NH02BK-R",
            "sku_name": "BH HIP HLSTR SZ 2 RH BLK",
            "cost": 7.9,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "2c31429e-567d-4f26-a388-e375cf697b93",
            "status": "Unallocated",
            "item_uuid": "16b47954-aecc-4af8-b293-bbcbde5a991f",
            "item_name": "AZOOM DUMMY ROUNDS 22 RIMFIRE 6/PK",
            "sku_uuid": "7dcf5f5e-49be-4437-a37f-3fb01f5a137a",
            "sku_id": "AZ12208",
            "sku_name": "AZOOM DUMMY ROUNDS 22 RIMFIRE 6/PK",
            "cost": 58.62,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "ac74dc1d-c146-4ceb-9c0a-7f8099b83ea5",
            "status": "Unallocated",
            "item_uuid": "60ae9274-e1b3-48f0-8b73-c678f04d1cbb",
            "item_name": "B/C SHT-N-C RND BULLSEYE TGT 60-6",
            "sku_uuid": "0032fd26-6c71-4f6d-9830-dcaf806a4875",
            "sku_id": "BC34550-60",
            "sku_name": "B/C SHT-N-C RND BULLSEYE TGT 60-6",
            "cost": 6.15,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "442d16db-86b2-4f07-8140-25311f22e80e",
            "status": "Unallocated",
            "item_uuid": "2b939a4d-95e2-45eb-9d64-556ef8396158",
            "item_name": "CAA QD VERTICAL GRIP W/COMPARTMENT",
            "sku_uuid": "f4334dc0-9946-499f-b115-eac2e9863f95",
            "sku_id": "CAABVG",
            "sku_name": "CAA QD VERTICAL GRIP W/COMPARTMENT",
            "cost": 44.34,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "fae35a8a-dc39-416e-82d2-57c8a34ab685",
            "status": "Unallocated",
            "item_uuid": "76dc2a5d-8e24-49b6-9712-ff0551248916",
            "item_name": "Women’s Ultra Fastpack III Mid GTX&#174;",
            "sku_uuid": "0c178ee0-a68b-4b38-8466-bc69c4c3ee24",
            "sku_id": "NF0A39IT4HW-060",
            "sku_name": "Women’s Ultra Fastpack III Mid GTX&#174;",
            "cost": 27.59,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "313d3f7f-b2ff-4e1f-806e-8fb11eea722d",
            "status": "Unallocated",
            "item_uuid": "feadbe40-b8c5-45ac-a9f0-330cef7023b1",
            "item_name": "Women’s Purist Triclimate&#174; Jacket",
            "sku_uuid": "5ec13524-1c45-45e5-bf5e-e5c1343133c9",
            "sku_id": "NF0A333ZXVR-XS",
            "sku_name": "Women’s Purist Triclimate&#174; Jacket",
            "cost": 87.12,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "8e9ca77b-7153-4a1b-8c14-86f344c174d5",
        "is_allocated": false,
        "purchase_order_id": "abe59ac4-7567-4021-9cc0-ab6cdfb3b3e2",
        "created_date": "2018-02-13T23:50:46.718353Z",
        "notes": "Nulla possimus ut repellendus ut.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "William Bender",
          "business_name": "Brown-Bennett",
          "address1": "56365 Christopher Parkway Suite 447\nLake Rebecca, WY 42773",
          "address2": "22972 Paul Walks\nEast Feliciafort, AK 24974-5772",
          "city": "Adamside",
          "state": "Vermont",
          "postal_code": "44746",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "31805724-1b61-4c64-98af-eceb730e1042",
            "status": "Unallocated",
            "item_uuid": "9e872a1e-723e-4260-9b11-a653acbce65a",
            "item_name": "Do-It Finesse Drop Shot Mold   3/16Oz FDS-8-316 3443",
            "sku_uuid": "421c8f8f-2778-4ce9-b28b-2a20878b421a",
            "sku_id": "034438",
            "sku_name": "Do-It Finesse Drop Shot Mold   3/16Oz FDS-8-316 3443",
            "cost": 14.3,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "333254de-6005-447f-8bc3-320d303b390b",
            "status": "Unallocated",
            "item_uuid": "5435537c-5a82-4eb8-a057-37806b80dd51",
            "item_name": "Men’s Pull-On Adventure Short",
            "sku_uuid": "70f4b3f8-8f27-4ee7-9dd0-be81c28f151f",
            "sku_id": "NF0A3FZF7D6-M-REG",
            "sku_name": "Men’s Pull-On Adventure Short",
            "cost": 21.92,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "b1820ef7-3b78-4d94-a932-9933082b1407",
            "status": "Unallocated",
            "item_uuid": "c9153a15-d8c0-48d0-94c2-5f52da722211",
            "item_name": "Men’s Long Sleeve Half Dome Tee",
            "sku_uuid": "44d96cf0-c040-4051-8f51-17f17fbc926d",
            "sku_id": "NF00CZY9UFC-S",
            "sku_name": "Men’s Long Sleeve Half Dome Tee",
            "cost": 4.6,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "3010972c-c74d-494d-973a-4c0db72a7700",
            "status": "Unallocated",
            "item_uuid": "72643531-4fb8-4b10-b075-7be1e49c3b70",
            "item_name": "Men’s Etip&#8482; Hardface Glove",
            "sku_uuid": "ce52d52e-6734-4932-8309-ffccb3e12eee",
            "sku_id": "NF0A2T7VZEF-M",
            "sku_name": "Men’s Etip&#8482; Hardface Glove",
            "cost": 76.38,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "5c9d02f2-dad0-4f99-8a52-0e31a4264633",
            "status": "Unallocated",
            "item_uuid": "42f2fac2-1982-44f1-9aa0-1d385496bca8",
            "item_name": "Men’s Trivert Pullover Hoodie",
            "sku_uuid": "5facc600-eff8-4e38-93c5-2acbb7bea4d3",
            "sku_id": "NF0A2ZMBRVA-M",
            "sku_name": "Men’s Trivert Pullover Hoodie",
            "cost": 60.53,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "fcf52274-1648-4526-b227-1d78f16640e7",
        "is_allocated": false,
        "purchase_order_id": "32AR9934",
        "created_date": "2018-02-13T23:50:47.197964Z",
        "notes": null,
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Kolton Weaver",
          "business_name": "Doba, Inc.",
          "address1": "3401 N Thanksgiving Way",
          "address2": "Suite 150",
          "city": "Lehi",
          "state": "UT",
          "postal_code": "84043",
          "phone_number": "801-765-6000"
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "2nd Day Air"
        },
        "line_items": [
          {
            "uuid": "8dc616fb-3b41-4c73-9106-e4cb900d932e",
            "status": "Unallocated",
            "item_uuid": "bbfc954c-1fe5-4f1a-89fa-db62b0d02c6c",
            "item_name": "ALLEN SCOPE SLEEVE 48\" CAMO",
            "sku_uuid": "0afd951c-152f-4d3e-ba1c-edae77ac25e4",
            "sku_id": "ALN123",
            "sku_name": "ALLEN SCOPE SLEEVE 48\" CAMO",
            "cost": 4.76,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
        "uuid": "97f730b9-dac5-4210-ba07-0b8436d81fe1",
        "is_allocated": false,
        "purchase_order_id": "b1b48203-4e3a-40f9-ac82-74f4f256df57",
        "created_date": "2018-02-13T23:50:47.233451Z",
        "notes": "Voluptate ducimus delectus odio non.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Michele Ramirez",
          "business_name": "Moss LLC",
          "address1": "281 Jones Curve Apt. 643\nLake Timothy, MA 28166",
          "address2": "7721 Estrada Plains\nWest Calebfurt, PW 58314",
          "city": "Port Troy",
          "state": "Montana",
          "postal_code": "67009",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "c7db915b-2f79-48b6-841c-65e173a9c243",
            "status": "Unallocated",
            "item_uuid": "6798538c-4cd6-4cdf-961f-851e8d08e52b",
            "item_name": "Minn Kota MKA-44 Telescopic Extension Handle (24-40 In.)",
            "sku_uuid": "e02b5039-13c9-4617-8df0-b956d38549d0",
            "sku_id": "031719",
            "sku_name": "Minn Kota MKA-44 Telescopic Extension Handle (24-40 In.)",
            "cost": 39.68,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "5e178aec-9e55-4bba-9ce8-6fe6541740ec",
            "status": "Unallocated",
            "item_uuid": "21a70257-8305-413c-866c-cca4b20a9011",
            "item_name": "BURRIS SIGN HIGH 1\" ZEE RINGS MATTE",
            "sku_uuid": "63c65211-32d8-42bd-a015-362c39207687",
            "sku_id": "BU420531",
            "sku_name": "BURRIS SIGN HIGH 1\" ZEE RINGS MATTE",
            "cost": 10.93,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "8cf50696-2fd5-442c-a605-be32f7938c69",
            "status": "Unallocated",
            "item_uuid": "4f07775c-54d5-4692-8bad-76d4fccd1c6e",
            "item_name": "Homestead Road Toter",
            "sku_uuid": "3703feb3-099d-44b1-aa63-70cadda246d3",
            "sku_id": "NF0A2SD1TRC-OS",
            "sku_name": "Homestead Road Toter",
            "cost": 71.71,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "13a0904b-0389-478e-9f2f-e1b527bb03dc",
        "is_allocated": false,
        "purchase_order_id": "f0a98e5d-afa2-4046-a7f2-b1ceb9b36141",
        "created_date": "2018-02-13T23:50:47.499419Z",
        "notes": "Consequatur eos qui fugit veniam voluptate vero maiores.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Tonya Shaw",
          "business_name": "Curtis-Bass",
          "address1": "584 Kaufman Crossroad\nNorth Juanberg, TN 09757-4026",
          "address2": "670 Moore Street Suite 309\nPort Julieborough, NH 19120-1967",
          "city": "Port Katherine",
          "state": "Alaska",
          "postal_code": "62775",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "057851c3-4bae-4c75-b12d-4eb6a9b9b4d5",
            "status": "Unallocated",
            "item_uuid": "49d4cea6-a60d-4632-9871-f5207ee1d8ce",
            "item_name": "CROSMAN .177 POINTED PELLETS 250/CD",
            "sku_uuid": "647b2db7-73e8-4cfb-b9aa-bea65c5adac3",
            "sku_id": "CRP177",
            "sku_name": "CROSMAN .177 POINTED PELLETS 250/CD",
            "cost": 16.64,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "4a5cc138-a902-4ebc-8c7e-f5b1d65f8d70",
            "status": "Unallocated",
            "item_uuid": "7b79be9e-24ba-474c-8779-0ef47e42dd03",
            "item_name": "Youth Flurry Wind Hoodie",
            "sku_uuid": "b97f8b15-d54c-4345-a611-6e411ae67f2c",
            "sku_id": "NF0A3BWO1F7-S",
            "sku_name": "Youth Flurry Wind Hoodie",
            "cost": 43.7,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "30aaa76d-946c-4485-a24e-a89d83b42c37",
            "status": "Unallocated",
            "item_uuid": "bb9d8d20-861f-409a-9534-8d939bdaf43b",
            "item_name": "Men’s Short Sleeve Half Dome Tee",
            "sku_uuid": "a35867c7-402b-4f23-b038-47d234b77289",
            "sku_id": "NF00CH2T1WB-L",
            "sku_name": "Men’s Short Sleeve Half Dome Tee",
            "cost": 86.9,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "24219b0b-ae2f-409a-9523-8ba04d7a9c06",
            "status": "Unallocated",
            "item_uuid": "435f3aee-5d46-49de-aeb4-2fa6d07f8c07",
            "item_name": "Men’s Resolve 2 Jacket",
            "sku_uuid": "b448e3ac-968a-41be-819a-2c9ffd89dddb",
            "sku_id": "NF0A2VD5LKM-S",
            "sku_name": "Men’s Resolve 2 Jacket",
            "cost": 58.23,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "0d7cfda0-6cd9-4b53-bbc7-9c765060eff8",
            "status": "Unallocated",
            "item_uuid": "539fb8d0-57d3-4827-9160-76bf763bf0ba",
            "item_name": "Toddler Girls’ Pulse Capri",
            "sku_uuid": "188c4c6b-2619-424f-be97-08c3b208f0bd",
            "sku_id": "NF0A3CT41QG-6T",
            "sku_name": "Toddler Girls’ Pulse Capri",
            "cost": 60.51,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "6c999ca0-3e4d-4e50-b333-92a1d56f57d9",
            "status": "Unallocated",
            "item_uuid": "6ad691cf-5109-426a-a65e-0c8fd4d06f9d",
            "item_name": "Women’s Struttin Jacket",
            "sku_uuid": "bee8bde6-3335-4a2c-863c-0104cfdc7263",
            "sku_id": "NF0A333MYDC-XS",
            "sku_name": "Women’s Struttin Jacket",
            "cost": 70.4,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "cfe04cd7-ef1a-4f23-bb61-5fb8f312880a",
        "is_allocated": false,
        "purchase_order_id": "5957d381-a4ab-4439-9022-96d2388ba1df",
        "created_date": "2018-02-13T23:50:48.177659Z",
        "notes": "Maiores vel deleniti modi accusamus excepturi.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Katherine Griffin",
          "business_name": "Liu-Suarez",
          "address1": "708 Nguyen Mission Suite 317\nLake James, FM 43637",
          "address2": "USNS Poole\nFPO AE 58621-0905",
          "city": "West Michele",
          "state": "Nevada",
          "postal_code": "44992",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "4a2f63cf-9442-45f7-8e9b-7abff19ab168",
            "status": "Unallocated",
            "item_uuid": "93a9e9d4-388b-4925-80fe-643dc2347888",
            "item_name": "Spyderco Ladybug 3 Purple FRN Plainedge",
            "sku_uuid": "41ec4434-254e-40cc-a85a-8b56c1dbb343",
            "sku_id": "004492",
            "sku_name": "Spyderco Ladybug 3 Purple FRN Plainedge",
            "cost": 21.7,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "3f77025c-6500-4651-904e-15bad12aa062",
            "status": "Unallocated",
            "item_uuid": "6927a6ab-5dcd-452a-9c31-c35ae99ac0bd",
            "item_name": "Do-It Finesse Drop Shot Mold   1/4Oz FDS-8-14 3444",
            "sku_uuid": "558e3968-6d63-4e69-8621-6788952d964c",
            "sku_id": "034445",
            "sku_name": "Do-It Finesse Drop Shot Mold   1/4Oz FDS-8-14 3444",
            "cost": 91.3,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "8f8e2937-5763-4ccf-afb4-f59ad4c84ae3",
            "status": "Unallocated",
            "item_uuid": "56fb888f-6f37-4c2c-9f12-9f34e6f4974e",
            "item_name": "CRKT M16-Z EDC 3\" BLK PLN",
            "sku_uuid": "c7b877d7-7523-4b79-8921-78ac61e85ef5",
            "sku_id": "CRKM16-01KZ",
            "sku_name": "CRKT M16-Z EDC 3\" BLK PLN",
            "cost": 85.84,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "514fcc4e-c649-4ee0-9bce-79c6da2cad12",
            "status": "Unallocated",
            "item_uuid": "27b7336e-e78c-4412-afa9-6026fa6177dd",
            "item_name": "Men’s Henley Tri-Blend Hoodie",
            "sku_uuid": "e6a0f14a-4ef9-4a78-a6ed-57263a4a94fc",
            "sku_id": "NF0A34Z42KY-M",
            "sku_name": "Men’s Henley Tri-Blend Hoodie",
            "cost": 27.41,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "9a280975-b3a8-486c-ba0f-8cf1d2b92b9b",
            "status": "Unallocated",
            "item_uuid": "f983d56e-78f4-489d-8c16-3b40dee14cce",
            "item_name": "Women’s Reactor Hoodie",
            "sku_uuid": "44032a5b-f923-4f99-a76f-21ca836c66f9",
            "sku_id": "NF0A2V9UUBG-M",
            "sku_name": "Women’s Reactor Hoodie",
            "cost": 77.4,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "ab132c6c-b2a1-4f59-bebc-bf5355b447f6",
            "status": "Unallocated",
            "item_uuid": "2dbd4c12-5a15-48d6-b671-2fa450e22abd",
            "item_name": "Men’s TKA 100 Glacier &#188; Zip",
            "sku_uuid": "94dd8a44-ad7e-470b-8b69-08b791b0c0f1",
            "sku_id": "NF00C744HCD-XL",
            "sku_name": "Men’s TKA 100 Glacier &#188; Zip",
            "cost": 7.51,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "79c39fbf-354a-45bd-b861-cfa5f6cb1f52",
        "is_allocated": false,
        "purchase_order_id": "9ceac4be-1b5a-46ac-bd30-dabd48bb17f1",
        "created_date": "2018-02-13T23:50:48.622388Z",
        "notes": "Reprehenderit hic fugiat officiis neque laborum omnis voluptates.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Dustin Clark",
          "business_name": "Sloan, Pierce and Warren",
          "address1": "40764 Miller Route\nMichaelview, NC 55742",
          "address2": "55510 Chapman Isle Apt. 369\nCynthiaborough, OR 32952",
          "city": "South Brookechester",
          "state": "Tennessee",
          "postal_code": "79092",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "431f8a11-db72-46f6-9521-9b5a6cce0ed5",
            "status": "Unallocated",
            "item_uuid": "4bfa8928-1f16-44ba-8d1f-f166844265c6",
            "item_name": "B/C SHT-N-C TGT ASSORT W TGT STAND",
            "sku_uuid": "bd132ec9-b2a1-4409-8657-0fd0802cae04",
            "sku_id": "BC34208",
            "sku_name": "B/C SHT-N-C TGT ASSORT W TGT STAND",
            "cost": 21.86,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "272d1b3f-313c-4580-a0c9-a660beb58d2c",
            "status": "Unallocated",
            "item_uuid": "44445f9e-0eef-4468-9b8c-d46bf1b0fca2",
            "item_name": "BTLR CRK FLIP SCOPE COVER 02 OBJ",
            "sku_uuid": "cb21642a-decf-4f5b-b9f2-9cd89608b682",
            "sku_id": "BTLR30020",
            "sku_name": "BTLR CRK FLIP SCOPE COVER 02 OBJ",
            "cost": 69.4,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "33b5fe7f-6c09-498b-bdad-aa36ea794011",
            "status": "Unallocated",
            "item_uuid": "eb795c3e-7061-49d8-85d0-391e10984729",
            "item_name": "Men’s Rarig Bib",
            "sku_uuid": "ce32cdc0-c681-4840-9701-731c39decb0e",
            "sku_id": "NF0A332HJK3-S-LNG",
            "sku_name": "Men’s Rarig Bib",
            "cost": 0.9,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "34ad369b-3e80-48fd-b970-41eb02427943",
            "status": "Unallocated",
            "item_uuid": "c62d858a-8c2f-43ae-9eb8-d36f06850c36",
            "item_name": "Men’s Short Sleeve Great Outdoors Tee",
            "sku_uuid": "497ca889-0ac1-4339-9768-d19e7a505ce3",
            "sku_id": "NF0A353H38X-S",
            "sku_name": "Men’s Short Sleeve Great Outdoors Tee",
            "cost": 32.92,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "4b128898-c01e-4255-9715-55783bfaae4a",
            "status": "Unallocated",
            "item_uuid": "b834c591-7dd1-44ca-a147-0c2d8ded4e47",
            "item_name": "Men’s Gatekeeper Pant",
            "sku_uuid": "d06246e4-ddf4-4ea7-a4ef-31ae25e00045",
            "sku_id": "NF0A332DJK3-XL-SHT",
            "sku_name": "Men’s Gatekeeper Pant",
            "cost": 96.95,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "0a86c2a9-18b8-4a72-8433-4d9a0de3f07e",
            "status": "Unallocated",
            "item_uuid": "94048220-a00c-4650-ba94-1550b9abfeeb",
            "item_name": "Men’s Short Sleeve Red Box Tee",
            "sku_uuid": "07e17865-510c-440f-872a-a1de67dee3f8",
            "sku_id": "NF00CA0F2TS-3XL",
            "sku_name": "Men’s Short Sleeve Red Box Tee",
            "cost": 72.84,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "2e449e10-8cc4-4426-a557-eb25ac1e423f",
            "status": "Unallocated",
            "item_uuid": "aa91eeef-a2f6-4fce-aa87-126711bea801",
            "item_name": "Boys’ ThermoBall&#8482; Full Zip Jacket",
            "sku_uuid": "f827dad1-b381-4a29-a484-9447deab4687",
            "sku_id": "NF0A34QHWYF-XS",
            "sku_name": "Boys’ ThermoBall&#8482; Full Zip Jacket",
            "cost": 61.48,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "21474dc3-7fc4-4c96-bf11-9b3043434fcf",
        "is_allocated": false,
        "purchase_order_id": "f839a593-0b3c-4270-8fc3-0f8c5eb809b6",
        "created_date": "2018-02-13T23:50:49.274353Z",
        "notes": "Commodi dolorem at asperiores ad soluta.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Linda Mueller",
          "business_name": "Long Ltd",
          "address1": "PSC 8832, Box 8132\nAPO AP 82153",
          "address2": "419 Lee Bridge Suite 614\nHelenside, CO 12041",
          "city": "Lake Maryhaven",
          "state": "Connecticut",
          "postal_code": "24817",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "a7a33b59-6c7e-44c6-a9c0-0696f25714d4",
            "status": "Unallocated",
            "item_uuid": "cc7eef79-353a-4973-bba4-0c6233563cae",
            "item_name": "ALLEN KNIT CAMO GUN SOCK 52\" GRN",
            "sku_uuid": "ecf5b755-c5c6-4fd4-a9f5-b2584d5a6c77",
            "sku_id": "ALN133",
            "sku_name": "ALLEN KNIT CAMO GUN SOCK 52\" GRN",
            "cost": 95.85,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "157e4587-3acb-4e0e-b3c6-9544a2c63745",
            "status": "Unallocated",
            "item_uuid": "8d3cc768-0d45-4b90-8a6c-cd91878a5904",
            "item_name": "Cold Steel Dragonfly Katana 88DK",
            "sku_uuid": "7c0bad1b-68dd-47b2-ab8e-a416f569dab7",
            "sku_id": "060145",
            "sku_name": "Cold Steel Dragonfly Katana 88DK",
            "cost": 68.23,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "c61c728a-0df9-41d9-baa3-f102fc4b0898",
            "status": "Unallocated",
            "item_uuid": "634be934-fc3e-4890-8259-cfc216c769d3",
            "item_name": "Tour Edge HT Max-J Junior Boys LH 5x2 Golf Set Age 9-12",
            "sku_uuid": "8e0499ee-2427-4a57-87a3-afe883d5420b",
            "sku_id": "1001544",
            "sku_name": "Tour Edge HT Max-J Junior Boys LH 5x2 Golf Set Age 9-12",
            "cost": 61.65,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "1ccec106-72f4-4dca-8674-5c2dd60c45ee",
            "status": "Unallocated",
            "item_uuid": "fce4d946-40f8-4cb1-90d3-7b8a73eac9f1",
            "item_name": "Women’s Novelty Nuptse Jacket",
            "sku_uuid": "9ae8baf4-e31d-4c09-8b10-7f70a4306be9",
            "sku_id": "NF0A33P8X80-L",
            "sku_name": "Women’s Novelty Nuptse Jacket",
            "cost": 55.81,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "ebb0d9c5-8718-4360-9f36-5b129ea42c7b",
            "status": "Unallocated",
            "item_uuid": "59637e85-ee2f-44a1-94b9-00f7ad2fcf6b",
            "item_name": "Boys’ Surgent Full Zip Hoodie",
            "sku_uuid": "fe1f233b-ab78-4dce-9689-25d282c4960d",
            "sku_id": "NF0A2U3UC7A-L",
            "sku_name": "Boys’ Surgent Full Zip Hoodie",
            "cost": 31.41,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "02bbe7a2-3e80-49dd-8942-748f194c90a1",
            "status": "Unallocated",
            "item_uuid": "143cf29f-f5d3-45a4-b164-c9ce899175eb",
            "item_name": "Trail Trucker",
            "sku_uuid": "93c223d3-d8f5-41b2-8f27-885997f0c0fe",
            "sku_id": "NF0A2ZEFXCG-OS",
            "sku_name": "Trail Trucker",
            "cost": 35.21,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "b8a99073-db84-40e3-ae31-b5c5f2eaee78",
        "is_allocated": false,
        "purchase_order_id": "4238bbca-400a-40d2-8392-65e81a43bf58",
        "created_date": "2018-02-13T23:50:49.741454Z",
        "notes": "Assumenda architecto eos molestiae maiores accusamus quos dicta.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Anne Lester",
          "business_name": "Davis-Jarvis",
          "address1": "564 Shawn Mountain\nEast Christineport, IL 35869-7532",
          "address2": "88039 Zachary Well Apt. 742\nSouth Jermaine, AK 61434-4862",
          "city": "Caldwellmouth",
          "state": "New York",
          "postal_code": "62765",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "e62d16c4-274b-4932-8c4f-81c2b7da764e",
            "status": "Unallocated",
            "item_uuid": "d593abaa-c215-46ac-938e-68648d13cc4f",
            "item_name": "Spyderco Atlantic Salt Knife   C89SYL",
            "sku_uuid": "28b50e93-81be-4139-bca7-4f371cebf692",
            "sku_id": "006892",
            "sku_name": "Spyderco Atlantic Salt Knife   C89SYL",
            "cost": 50.54,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "195559ab-f6f7-4ab0-8019-bdb1f63a4898",
            "status": "Unallocated",
            "item_uuid": "72e16bf1-c19e-42b8-b9ca-b9116c3a979f",
            "item_name": "BH RFL BANDOLEER (6) BLK",
            "sku_uuid": "8d01803a-9714-459d-ad03-f7497d8596b3",
            "sku_id": "BH55SOS1BK",
            "sku_name": "BH RFL BANDOLEER (6) BLK",
            "cost": 81.3,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "0cd28fca-e434-4277-8e86-6a9fe05c0e3c",
            "status": "Unallocated",
            "item_uuid": "c7c4f7eb-2943-4227-bedf-ca0d6963e370",
            "item_name": "FED PWRSHK 300WSM 180GR SP 20/200",
            "sku_uuid": "d760cbb9-c16e-46b5-8f1d-955b585e9067",
            "sku_id": "FE300WSMC",
            "sku_name": "FED PWRSHK 300WSM 180GR SP 20/200",
            "cost": 90.5,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "7657f449-1735-41ba-8734-f6b88300d9c7",
            "status": "Unallocated",
            "item_uuid": "822f9ca7-5649-4fbf-84d9-5c4e7fef3b65",
            "item_name": "CCI 17HMR 20GR FMJ 50/2000",
            "sku_uuid": "26fd3373-9f15-4b0e-9e65-76618a89b7ea",
            "sku_id": "CCI55",
            "sku_name": "CCI 17HMR 20GR FMJ 50/2000",
            "cost": 29.81,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "3c193b3d-d273-4df7-af39-ab4af7596092",
            "status": "Unallocated",
            "item_uuid": "2f2d3dd3-67c9-40e0-a4e3-5364a3a3cdee",
            "item_name": "BH SOCOM PSTL CS BLK",
            "sku_uuid": "52f80c45-a7e8-4a22-8aac-9158495ec440",
            "sku_id": "BH66SS00BK",
            "sku_name": "BH SOCOM PSTL CS BLK",
            "cost": 67.6,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "edd9c8ed-8fad-4575-9e73-8050928474a3",
            "status": "Unallocated",
            "item_uuid": "2fbd08e8-bdc6-4d9e-9937-f9ff1d3da9af",
            "item_name": "Boys’ Mid Cloud Fleece Hoodie",
            "sku_uuid": "cb5626f0-72e1-4f5d-86f0-7d099a6f3d60",
            "sku_id": "NF0A3CPKZBT-L",
            "sku_name": "Boys’ Mid Cloud Fleece Hoodie",
            "cost": 61.52,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "dad7d8d1-831b-4b8c-b430-df0cfc99d8d9",
            "status": "Unallocated",
            "item_uuid": "7a5f9ae9-75b6-4d01-8f99-cc2527518365",
            "item_name": "Girls’ Warm Storm Jacket",
            "sku_uuid": "52a66853-9ec7-4db1-80cc-75512d88df36",
            "sku_id": "NF0A34UXRWW-XS",
            "sku_name": "Girls’ Warm Storm Jacket",
            "cost": 46.97,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "e7b62684-0bf3-4534-980a-d3c41b9c3936",
            "status": "Unallocated",
            "item_uuid": "76a96c6f-6434-4467-a8b4-a6634c94d1ae",
            "item_name": "Girls’ Oso Fleece Pullover",
            "sku_uuid": "f4ca5e3d-0767-4b10-bb5d-c3dbdf907367",
            "sku_id": "NF0A34TWJK3-L",
            "sku_name": "Girls’ Oso Fleece Pullover",
            "cost": 84.39,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "267ef381-1237-4aef-8fb7-722dc09001eb",
            "status": "Unallocated",
            "item_uuid": "c6048fdc-dc36-4b01-9498-e80e3ed4d5d7",
            "item_name": "Infant Reversible Perrito Jacket",
            "sku_uuid": "13108f00-710e-4288-82b0-c712739a2041",
            "sku_id": "NF0A34WCPKC-12M",
            "sku_name": "Infant Reversible Perrito Jacket",
            "cost": 43.14,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "0b524691-7fd1-4332-918e-575a09b44f92",
        "is_allocated": false,
        "purchase_order_id": "2a73d6ee-593c-4621-831f-cf34ad1bd785",
        "created_date": "2018-02-13T23:50:50.553960Z",
        "notes": "Dignissimos quia modi ratione hic architecto doloribus.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Daniel Reid",
          "business_name": "Hodges-Patterson",
          "address1": "27006 Pineda Ports\nPort Sandra, ME 46520",
          "address2": "96245 Salas Summit\nEast Karen, NH 47364",
          "city": "East Robert",
          "state": "Wisconsin",
          "postal_code": "32921",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "42e5dbe1-d46a-4164-826b-d77f03cba3fe",
            "status": "Unallocated",
            "item_uuid": "2169f133-0ee8-4430-917c-255c6d9595a6",
            "item_name": "Frogg Toggs Pilot Frogg Guide Bib Stone/Taupe - Large",
            "sku_uuid": "a45f5cd9-2e3c-4886-860f-b46cee114f21",
            "sku_id": "1002545",
            "sku_name": "Frogg Toggs Pilot Frogg Guide Bib Stone/Taupe - Large",
            "cost": 4.75,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "cec89f19-8be3-4a47-a7a0-c0400b4f4eb9",
            "status": "Unallocated",
            "item_uuid": "25a337fa-ce62-4a31-9548-95c4a3d08986",
            "item_name": "BH SERPA CQC BL/PDL CF FOR G26 LH BK",
            "sku_uuid": "f8ce0d82-8f64-4d48-a8f7-d272a2673300",
            "sku_id": "BH410001BK-L",
            "sku_name": "BH SERPA CQC BL/PDL CF FOR G26 LH BK",
            "cost": 76.6,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "7011ad0e-8327-45bf-95b8-ccb3c04f67b4",
            "status": "Unallocated",
            "item_uuid": "759838c8-5d37-4a43-a664-809f45852b7b",
            "item_name": "AZOOM SNAP CAPS 308WIN 2/PK",
            "sku_uuid": "30496d86-236e-4d9e-924c-de8890c39494",
            "sku_id": "AZ12228",
            "sku_name": "AZOOM SNAP CAPS 308WIN 2/PK",
            "cost": 50.79,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "b8141949-36ad-44f5-a20d-b9ab923b002d",
            "status": "Unallocated",
            "item_uuid": "05a1a9fb-e065-48a8-b58e-02e0f317a5ec",
            "item_name": "NAP Black Apache EQ Stabilizer",
            "sku_uuid": "b3798830-ba91-46bd-a43b-d5d1b7505a0d",
            "sku_id": "1000543",
            "sku_name": "NAP Black Apache EQ Stabilizer",
            "cost": 86.16,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "bbdaefee-d3c2-49e5-ade6-a96c26615fa1",
            "status": "Unallocated",
            "item_uuid": "e47852d3-4337-4a3c-8c60-3dacd1b5f0cc",
            "item_name": "Cold Steel Trail Master San Mai III 16JSM",
            "sku_uuid": "6afe0ecd-f9c0-428f-b8b5-4ccc4e23240f",
            "sku_id": "001805",
            "sku_name": "Cold Steel Trail Master San Mai III 16JSM",
            "cost": 27.78,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "53c8b0e1-06f4-4b48-add3-218762bbbf5a",
            "status": "Unallocated",
            "item_uuid": "089257b9-dc4e-4d37-906a-8620145e83e9",
            "item_name": "Women’s Long Sleeve In-A-Flash Raglan Tee",
            "sku_uuid": "acc43022-6576-4289-9eca-b02e0d7ecb35",
            "sku_id": "NF0A3BBP7D6-S",
            "sku_name": "Women’s Long Sleeve In-A-Flash Raglan Tee",
            "cost": 8.86,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "e393bc66-bef6-487c-9703-734723fae079",
            "status": "Unallocated",
            "item_uuid": "d66505ce-3280-451e-abef-fb5ab0071efd",
            "item_name": "Boys’ Gordon Lyons &#188; Zip",
            "sku_uuid": "80b7dcc1-ed75-41ef-9edb-6884c2fba627",
            "sku_id": "NF0A34S4DYY-XL",
            "sku_name": "Boys’ Gordon Lyons &#188; Zip",
            "cost": 70.34,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "d43c2bc2-f4f1-4706-9cb6-4b5e4662b090",
            "status": "Unallocated",
            "item_uuid": "48da8c8f-dbaa-4e28-a5fc-7ab88e0d8524",
            "item_name": "Women’s One Trail",
            "sku_uuid": "3f25b2ce-c1ff-4575-8d44-ccf4f7d28302",
            "sku_id": "NF0A39I84HB-105",
            "sku_name": "Women’s One Trail",
            "cost": 34.58,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "b7ddfc45-fa01-4874-bbaf-84aa02075d84",
        "is_allocated": false,
        "purchase_order_id": "652ef908-d2e6-4092-a802-05b0b263654e",
        "created_date": "2018-02-13T23:50:51.237863Z",
        "notes": "Veritatis voluptates nesciunt similique fugit veritatis.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Julian Hicks",
          "business_name": "Alexander-Ward",
          "address1": "706 Woods Bridge\nRobertsville, IL 53025",
          "address2": "4011 Anderson Way Apt. 183\nNew Madison, WI 09249",
          "city": "Lake Karenview",
          "state": "Rhode Island",
          "postal_code": "50014",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "f8bffa63-6212-4224-ad48-23df14e4593a",
            "status": "Unallocated",
            "item_uuid": "6991c2c5-4e2f-4566-a0db-fb3d99fc06d4",
            "item_name": "DMT Diafold Serrated Fine      FSKF",
            "sku_uuid": "52256811-a1ac-4229-9b76-e167375f6636",
            "sku_id": "011055",
            "sku_name": "DMT Diafold Serrated Fine      FSKF",
            "cost": 25.51,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "1b6121a5-5c1f-46d9-beb1-ee5ab97788d3",
            "status": "Unallocated",
            "item_uuid": "7daa2aa3-af44-49ff-a72b-9d6eaa9a0898",
            "item_name": "Plano Bow Max Cross Bow Case Black 1133-00",
            "sku_uuid": "29c7e625-9bd1-443f-b4f3-2537ec1e63f8",
            "sku_id": "011334",
            "sku_name": "Plano Bow Max Cross Bow Case Black 1133-00",
            "cost": 95.43,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "6542888d-9474-435e-883a-748b5b80729b",
            "status": "Unallocated",
            "item_uuid": "7dd92eed-35e8-4a17-80a6-a73a35c9501c",
            "item_name": "Girls’ East Ridge Triclimate&#174;",
            "sku_uuid": "fd2306db-e196-4d6f-b6ae-0865796e80aa",
            "sku_id": "NF0A34UVP71-XXS",
            "sku_name": "Girls’ East Ridge Triclimate&#174;",
            "cost": 20.1,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "29df3eef-3db2-4e8d-82ce-6eb4c0518bec",
            "status": "Unallocated",
            "item_uuid": "01c5de68-2a05-4fc8-b955-e18dfcfa4ec7",
            "item_name": "Men’s L/S Have You Herd Well-Loved Cotton Tee",
            "sku_uuid": "897abd97-d5cd-4bff-b38d-a4a00b97503f",
            "sku_id": "NF0A3FQ8WXG-M",
            "sku_name": "Men’s L/S Have You Herd Well-Loved Cotton Tee",
            "cost": 35.7,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "0301cfc8-bb73-431f-b2a1-ce8003ef8adf",
            "status": "Unallocated",
            "item_uuid": "f3184619-b62e-4e70-95ce-a95be02c97c3",
            "item_name": "Women’s Ultra Fastpack III GTX&#174;",
            "sku_uuid": "972d06ad-dae1-4d4b-9312-92f8e440c397",
            "sku_id": "NF0A39IS1XV-065",
            "sku_name": "Women’s Ultra Fastpack III GTX&#174;",
            "cost": 26.26,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "55038a67-fd12-417e-9331-0ff662fa3187",
            "status": "Unallocated",
            "item_uuid": "4863bea5-50ae-45e0-8fc8-2e7083fccd31",
            "item_name": "Men’s Cali Roots Fleece Crew",
            "sku_uuid": "2d31b495-d130-4628-aa6e-6bc3cb0e7282",
            "sku_id": "NF0A356PJK3-L",
            "sku_name": "Men’s Cali Roots Fleece Crew",
            "cost": 0.94,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "86aff3c0-e5e3-4531-aff5-5b9db1c71773",
        "is_allocated": false,
        "purchase_order_id": "9d5a8376-d3a6-4247-8e38-a610b5acb1bb",
        "created_date": "2018-02-13T23:50:51.963536Z",
        "notes": "Omnis consequuntur esse a numquam possimus.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Michael Wagner",
          "business_name": "Kidd, Cooke and Calhoun",
          "address1": "85904 Rhonda Road Apt. 987\nPort Susanburgh, MT 80708-8130",
          "address2": "5222 Stevens Courts\nSouth Andreaville, ME 54880",
          "city": "North Dylanland",
          "state": "Texas",
          "postal_code": "37558",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "b13169df-4e98-4827-846c-f48fb871c801",
            "status": "Unallocated",
            "item_uuid": "fcb5a296-6dd8-4365-8e2e-303bdd261774",
            "item_name": "BTLR CRK FLIP SCOPE COVER 21 OBJ",
            "sku_uuid": "e471d63b-f576-4b09-a806-ceb783fd7070",
            "sku_id": "BTLR30210",
            "sku_name": "BTLR CRK FLIP SCOPE COVER 21 OBJ",
            "cost": 1.2,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "c8773680-c3e2-4dd8-9f6e-fb8a833db9e6",
            "status": "Unallocated",
            "item_uuid": "0fa9d912-bfce-4e9e-a81a-edb2309eaaec",
            "item_name": "CORBON DPX 40SW 140GR BRNS X 20/500",
            "sku_uuid": "f5ef762e-820a-4c20-b98e-57c7a5e8f17d",
            "sku_id": "CORDPX40140",
            "sku_name": "CORBON DPX 40SW 140GR BRNS X 20/500",
            "cost": 24.43,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "233b4ac1-ac31-4c51-9275-a3e936535506",
            "status": "Unallocated",
            "item_uuid": "ac874a9b-84ec-4895-ab04-ec036f4653e9",
            "item_name": "Frogg Toggs Pilot Pant Black/Charcoal - Medium",
            "sku_uuid": "9b7ab262-85ab-487d-8dfa-64120f13e5e4",
            "sku_id": "1002556",
            "sku_name": "Frogg Toggs Pilot Pant Black/Charcoal - Medium",
            "cost": 35.71,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "231b53f0-a68d-45d2-aeea-687f8fcebb63",
            "status": "Unallocated",
            "item_uuid": "c0cc6dcf-92c8-49eb-a751-51024d7cec96",
            "item_name": "Cold Steel Trail Hawk 90TH",
            "sku_uuid": "d1a925a7-22b2-4d99-afe0-d702313cfef1",
            "sku_id": "003991",
            "sku_name": "Cold Steel Trail Hawk 90TH",
            "cost": 71.4,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "3068a1e7-5dff-41ac-90d3-1f1aac401500",
            "status": "Unallocated",
            "item_uuid": "a4bbef18-ae77-4888-8691-c6c353ff8b27",
            "item_name": "Limbsaver Airtech Recoil Pad Remington 700 ADL/BDL ML",
            "sku_uuid": "3e33230f-df6f-41dc-8c91-2024b18d4236",
            "sku_id": "1000816",
            "sku_name": "Limbsaver Airtech Recoil Pad Remington 700 ADL/BDL ML",
            "cost": 89.98,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "845aacd1-8c02-4b02-a01a-d2c16b8374a1",
            "status": "Unallocated",
            "item_uuid": "12dd8cfe-a163-4187-86fc-7896e1177881",
            "item_name": "Boys’ Chimborazo Hoodie",
            "sku_uuid": "30101f09-8833-4b18-9fd6-ce4f26c6987c",
            "sku_id": "NF00A7ASH7H-S",
            "sku_name": "Boys’ Chimborazo Hoodie",
            "cost": 92.17,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "8becd520-9b38-416a-a842-1e66a07299ef",
            "status": "Unallocated",
            "item_uuid": "48d9ed10-d7e4-4208-992e-1ff3a8cb0421",
            "item_name": "Women’s Fave Lite Half Dome Full Zip Hoodie",
            "sku_uuid": "dc359716-2b4c-4fcb-9cca-74267d6a3141",
            "sku_id": "NF0A2ZMDXAB-XXL",
            "sku_name": "Women’s Fave Lite Half Dome Full Zip Hoodie",
            "cost": 20.27,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "d1ee8ad4-6a51-4ca4-9be6-a82162891ebd",
            "status": "Unallocated",
            "item_uuid": "0952c88f-7675-4426-b16f-161537e56fd6",
            "item_name": "Men’s Ventrix&#8482; Hoodie",
            "sku_uuid": "34fc528b-6768-4ecc-a89a-944fdb56513c",
            "sku_id": "NF0A39NDWGP-S",
            "sku_name": "Men’s Ventrix&#8482; Hoodie",
            "cost": 6.21,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "9a64ec94-45d1-41fe-98ac-7c5fc28b416c",
        "is_allocated": false,
        "purchase_order_id": "f5a487a0-8d19-41ec-9c9d-feccc7f8f551",
        "created_date": "2018-02-13T23:50:52.524902Z",
        "notes": "Nostrum dignissimos quia ipsum error aperiam cum.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Amber Rollins",
          "business_name": "Nichols-Brown",
          "address1": "2321 Soto Fall Suite 673\nKathleenview, AZ 76164-4116",
          "address2": "26562 Katherine Oval Apt. 181\nMeganfort, OH 69362-9386",
          "city": "Bellview",
          "state": "Alaska",
          "postal_code": "36574",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "a757f684-5d6e-4f41-9905-09841e0776ac",
            "status": "Unallocated",
            "item_uuid": "d01e29f5-d0e1-409a-a725-2cbfd81554ab",
            "item_name": "BH HIP HLSTR SZ 5 LH BLK",
            "sku_uuid": "895f14de-0a7d-4d4f-a596-0fb059f12317",
            "sku_id": "BH73NH05BK-L",
            "sku_name": "BH HIP HLSTR SZ 5 LH BLK",
            "cost": 69.83,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "f29b71d0-fd5a-4488-899c-614bfa7580ad",
            "status": "Unallocated",
            "item_uuid": "e6b9adb4-837f-4e37-8d2f-0a273181f571",
            "item_name": "Meprolight Glock G26/G27 G/O Fixed Set TD",
            "sku_uuid": "1acb5158-22f3-4184-bbc9-c2a157bd4559",
            "sku_id": "1001926",
            "sku_name": "Meprolight Glock G26/G27 G/O Fixed Set TD",
            "cost": 7.5,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "a0b8cf17-af98-4e7e-ba63-7ad2530de46f",
            "status": "Unallocated",
            "item_uuid": "ef7e6138-91a4-4d4d-8419-91fed6c0818f",
            "item_name": "Minn Kota MKR-19 Circuit Breaker",
            "sku_uuid": "cc36c2fe-10e5-4e7e-a2c7-0dad2e264427",
            "sku_id": "023554",
            "sku_name": "Minn Kota MKR-19 Circuit Breaker",
            "cost": 34.59,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "dd6b33a8-d967-4a48-ad5d-876049309af3",
            "status": "Unallocated",
            "item_uuid": "d5be639b-837f-4eda-b9ef-fbe2c1f06957",
            "item_name": "BH SERPA LEVEL 2 DUTY 1911 RH BLK",
            "sku_uuid": "fcf26ae6-1825-44b8-a21f-bae51569de0f",
            "sku_id": "BH44H003BK-R",
            "sku_name": "BH SERPA LEVEL 2 DUTY 1911 RH BLK",
            "cost": 65.48,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "15d61898-4bd7-46fc-ae6b-9665e9ef44f1",
            "status": "Unallocated",
            "item_uuid": "07b2b684-c6cf-4052-8aac-e977b0d97e70",
            "item_name": "SPR GOLD DOT 357MAG 125GR HP 20/500",
            "sku_uuid": "3c3511a9-d147-4bef-898a-4fdb0ed2e828",
            "sku_id": "CCI23920",
            "sku_name": "SPR GOLD DOT 357MAG 125GR HP 20/500",
            "cost": 14.48,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "53b80bc9-46f3-40fd-be64-2ed317b3de83",
            "status": "Unallocated",
            "item_uuid": "531278fe-bfa7-461e-aaa5-7dc5bfdcb46d",
            "item_name": "TNF One Touch Lite Trucker",
            "sku_uuid": "bbf1a1ef-036f-46e8-8a1b-a34581ef18f5",
            "sku_id": "NF0A3FJRVJY-OS",
            "sku_name": "TNF One Touch Lite Trucker",
            "cost": 53.59,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "128d6e5c-8fc1-496f-9ab5-3ec8f39ae1e6",
            "status": "Unallocated",
            "item_uuid": "c2ff71f4-7344-4fe2-b865-05bcf5e36649",
            "item_name": "Men’s ThermoBall&#8482; Traction Mule IV",
            "sku_uuid": "c1e83cec-629d-4ec9-94fc-8a16b12186eb",
            "sku_id": "NF0A331EYWU-100",
            "sku_name": "Men’s ThermoBall&#8482; Traction Mule IV",
            "cost": 15.32,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "4454430a-943c-4ddc-9f80-ad9e10fc7b9a",
        "is_allocated": false,
        "purchase_order_id": "2e5582c0-7bd5-48ea-84c8-ce0f5b6fb2c9",
        "created_date": "2018-02-13T23:50:53.081619Z",
        "notes": "Quis recusandae perspiciatis quod impedit iure ex.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Ronald Fletcher",
          "business_name": "Rodriguez, Whitaker and Shields",
          "address1": "613 Castaneda Forks Apt. 870\nEast Donnachester, SD 16046",
          "address2": "62784 Wendy Plaza Suite 814\nEast Michelebury, WI 97104-3813",
          "city": "Lake Ashley",
          "state": "Vermont",
          "postal_code": "29832",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "95c93f26-d4b4-4b11-89c9-fb2b4cb42642",
            "status": "Unallocated",
            "item_uuid": "81315e1c-ffdc-4d60-b966-fa2ac0a02869",
            "item_name": "CCI/BLAZER 9MM 115GR FMJ 50/1000",
            "sku_uuid": "6152315a-4ac5-4ffc-9283-b9be67770dd1",
            "sku_id": "CCI3509",
            "sku_name": "CCI/BLAZER 9MM 115GR FMJ 50/1000",
            "cost": 34.75,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "0a1e8ce0-0977-404a-b797-358b079623c0",
            "status": "Unallocated",
            "item_uuid": "acfbe324-e2d9-4f4a-bb66-7016717b8a0a",
            "item_name": "Rawlings Little League Competition Grade Baseball 1 Dozen",
            "sku_uuid": "f30bcb03-dbda-40fa-aad8-bccf2dad00e2",
            "sku_id": "1002364",
            "sku_name": "Rawlings Little League Competition Grade Baseball 1 Dozen",
            "cost": 83.39,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "bb08c3df-23c4-4b7e-afb9-4ed88f08677f",
            "status": "Unallocated",
            "item_uuid": "a5e110b3-32ac-4747-9e19-0d33b537a23e",
            "item_name": "CZ 1\" RINGS EURO 452/511 11MM DT",
            "sku_uuid": "d4080a94-4f5d-49d5-9d81-aa3e03fda733",
            "sku_id": "CZ19001",
            "sku_name": "CZ 1\" RINGS EURO 452/511 11MM DT",
            "cost": 50.8,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "cd783ec9-d9b2-445d-bf7b-56281cf628f8",
            "status": "Unallocated",
            "item_uuid": "4a81f0d3-9d4f-4a6e-9ba1-1e8bba89f2ad",
            "item_name": "FED PWRSHK 303BRIT 150GR SP 20/200",
            "sku_uuid": "879a4d00-198c-448f-9e31-a05ef60323eb",
            "sku_id": "FE303B",
            "sku_name": "FED PWRSHK 303BRIT 150GR SP 20/200",
            "cost": 37.94,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "679c5f45-d400-41a3-a78b-670ad0453906",
            "status": "Unallocated",
            "item_uuid": "31d82072-b0e1-4a4e-b336-43bfb7bab8b0",
            "item_name": "CCI 22WMR SHOTSHELL 20/2000",
            "sku_uuid": "13fa9855-e22c-4112-8736-013104adc1d9",
            "sku_id": "CCI25",
            "sku_name": "CCI 22WMR SHOTSHELL 20/2000",
            "cost": 66.34,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "bc0deb9f-942c-49e5-9fa9-b248bdf34946",
            "status": "Unallocated",
            "item_uuid": "6d0894b0-f8f9-432c-895d-b10ca2020b47",
            "item_name": "Women’s Novelty Nuptse Vest",
            "sku_uuid": "0995e83b-8890-4450-a128-4d6a00cf6d01",
            "sku_id": "NF0A35D6374-XS",
            "sku_name": "Women’s Novelty Nuptse Vest",
            "cost": 47.78,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "e39bc7d8-a6a9-44c7-979e-d9972dc5b9c5",
            "status": "Unallocated",
            "item_uuid": "906b035b-b8fc-4ab0-ba85-cd0da735136c",
            "item_name": "Women’s Fave Half Dome Full Zip Hoodie",
            "sku_uuid": "42edcfed-a142-4efb-b574-1546c068dfef",
            "sku_id": "NF0A2THUWUW-XL",
            "sku_name": "Women’s Fave Half Dome Full Zip Hoodie",
            "cost": 74.17,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "78ad3ed9-0451-4a4d-a163-b39682d65d14",
            "status": "Unallocated",
            "item_uuid": "b6b0595a-fd85-4b85-8957-998c669e4c04",
            "item_name": "Women’s Motivation Stripe Tank",
            "sku_uuid": "ef564cb9-a62c-4357-8069-733b62be88f9",
            "sku_id": "NF0A3LMB5FW-S",
            "sku_name": "Women’s Motivation Stripe Tank",
            "cost": 28.72,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "fc11f11a-7005-4ede-88da-707770485a23",
        "is_allocated": false,
        "purchase_order_id": "b1267b2e-3267-4b8d-8059-ebf0df06cca7",
        "created_date": "2018-02-13T23:50:53.763386Z",
        "notes": "Nostrum earum dolorum quo eos rerum cum quam minima.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Andrew Mann",
          "business_name": "Lane Inc",
          "address1": "320 Caleb Square Apt. 848\nFuentesfort, CT 69640",
          "address2": "USNV Lloyd\nFPO AA 30117-1579",
          "city": "North Eric",
          "state": "South Carolina",
          "postal_code": "38005",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "28e1d919-a0b3-45a1-8c0e-38a4a53f1900",
            "status": "Unallocated",
            "item_uuid": "476d46eb-f25f-45e0-87e5-a98a6647548c",
            "item_name": "Barnett Crossbows Crank Cocking Device",
            "sku_uuid": "5d840949-d4b0-45c3-8444-ebe296b65ba2",
            "sku_id": "1001463",
            "sku_name": "Barnett Crossbows Crank Cocking Device",
            "cost": 32.29,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "ba93bd55-4edb-4a31-bfd0-f952cb86dcfb",
            "status": "Unallocated",
            "item_uuid": "d03c79cd-de94-448a-aa98-5db50f271942",
            "item_name": "BULLDOG EXTREME FOR GLK 29/30/36",
            "sku_uuid": "03fd5e66-1c1b-470f-8a72-5e27474e598b",
            "sku_id": "BDFSN-33",
            "sku_name": "BULLDOG EXTREME FOR GLK 29/30/36",
            "cost": 29.95,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "fd65105a-3cc6-47a2-9931-f6b0b3c4f6b0",
            "status": "Unallocated",
            "item_uuid": "05824f5c-8280-42e9-b8e4-78c224d0544b",
            "item_name": "FAB Defense Pentagon Magazine Coupler for 5- 10rd Ultimags",
            "sku_uuid": "f7c7a07c-1ca3-4c60-ae07-e84976bd01a6",
            "sku_id": "1001908",
            "sku_name": "FAB Defense Pentagon Magazine Coupler for 5- 10rd Ultimags",
            "cost": 65.38,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "23eb1b7c-1e1e-4acd-8bac-e2519d786769",
            "status": "Unallocated",
            "item_uuid": "a20a5660-a5a1-403f-b35f-5eade2ba3375",
            "item_name": "Men’s Climb On Full Zip Hoodie",
            "sku_uuid": "60fbc94b-4279-4b64-bb87-101b4b94b4f3",
            "sku_id": "NF0A34Z1E2C-M",
            "sku_name": "Men’s Climb On Full Zip Hoodie",
            "cost": 52.93,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "fd59f12b-d3cc-4059-a1ba-7ca1bea9fbd3",
            "status": "Unallocated",
            "item_uuid": "770c768d-c0ac-4653-8886-16d3135d2bda",
            "item_name": "Girls’ S/S Reaxion 2.0 Tee",
            "sku_uuid": "f9f2e8a3-8101-4628-b7a9-1b304ca7cde4",
            "sku_id": "NF0A3CULUAX-XL",
            "sku_name": "Girls’ S/S Reaxion 2.0 Tee",
            "cost": 70.8,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "4d31b364-0384-4b06-b662-44db1e8b849f",
        "is_allocated": false,
        "purchase_order_id": "a3fd81d4-e7cf-4a7e-8437-9eed90f8ce4a",
        "created_date": "2018-02-13T23:50:54.259266Z",
        "notes": "Rerum molestias praesentium aspernatur explicabo aliquid dolores reiciendis eveniet.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Sarah Sparks",
          "business_name": "Nguyen, Lee and Michael",
          "address1": "59202 Harrington Shore\nCameronland, ND 74072-3375",
          "address2": "USCGC Henry\nFPO AA 49805-6894",
          "city": "South Dylan",
          "state": "Michigan",
          "postal_code": "77511",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "3ce9d75d-d506-45f9-8010-94bdcccd50e0",
            "status": "Unallocated",
            "item_uuid": "d49ab4cf-7e5a-4e20-8020-aa30df5fdbe3",
            "item_name": "BH INSIDE PANT HLSTR SZ 5 LH BLK",
            "sku_uuid": "d089bb16-9231-4a00-8fc7-82c8467f4396",
            "sku_id": "BH73IP05BK-L",
            "sku_name": "BH INSIDE PANT HLSTR SZ 5 LH BLK",
            "cost": 48.71,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "b63ee3cb-8031-4752-b4e0-2776806c5a11",
            "status": "Unallocated",
            "item_uuid": "4d49ff8f-98b1-42a7-bf8f-931fee557091",
            "item_name": "Women’s Insulated Ancha Parka",
            "sku_uuid": "2a35771d-f5ec-4a56-ba31-b44a9899c8a1",
            "sku_id": "NF00CG1BJK3-XXL",
            "sku_name": "Women’s Insulated Ancha Parka",
            "cost": 42.97,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "8710dfed-7867-4648-b503-b840e8400aee",
        "is_allocated": false,
        "purchase_order_id": "a6fffe6d-3e5c-434c-8578-d7a7fe310c44",
        "created_date": "2018-02-13T23:50:54.443711Z",
        "notes": "Non voluptates distinctio assumenda eligendi.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Chad Whitney",
          "business_name": "Clark-Rasmussen",
          "address1": "5742 Johnson Drives\nSouth Lorettaport, HI 33938",
          "address2": "0981 Christian Fall\nNew Philipview, RI 54582",
          "city": "West Deborah",
          "state": "Nebraska",
          "postal_code": "91517",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "31b7e7a1-1cff-4394-a6d2-2e448bcd997a",
            "status": "Unallocated",
            "item_uuid": "8095fcb0-97ec-4a8e-a9ab-c3e936bf7939",
            "item_name": "BH NEOPRENE ELBOW PAD BLK",
            "sku_uuid": "37bad60e-a0f7-416f-aa9b-6b221d37dccd",
            "sku_id": "BH809200BK",
            "sku_name": "BH NEOPRENE ELBOW PAD BLK",
            "cost": 23.53,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "8637293d-1141-4f8a-917c-c142ec0ddb95",
            "status": "Unallocated",
            "item_uuid": "1b0b0cdc-6ae2-45a2-b318-192e8383de9f",
            "item_name": "Spyderco Military Model Camo G-10 Plainedge C36GPCM",
            "sku_uuid": "86331b9b-5b3f-4026-a5c4-967f5c718775",
            "sku_id": "003341",
            "sku_name": "Spyderco Military Model Camo G-10 Plainedge C36GPCM",
            "cost": 82.98,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "04141f7e-ed87-4801-a006-04fa218502ef",
            "status": "Unallocated",
            "item_uuid": "6a03102e-1571-4fdd-b3a6-2f105d5ed075",
            "item_name": "BULLDOG EXTREME M/L AUTO FOR GLK 17",
            "sku_uuid": "9c17c00c-6474-4f7d-b581-87bdbc560815",
            "sku_id": "BDFSN-7",
            "sku_name": "BULLDOG EXTREME M/L AUTO FOR GLK 17",
            "cost": 51.24,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "17a15aca-68b5-4478-b542-53493888d4d3",
            "status": "Unallocated",
            "item_uuid": "850dccbb-dc77-423e-9e00-9654cf176e50",
            "item_name": "B/C SHT-N-C RND BULLSEYE TGT 30-8",
            "sku_uuid": "dc7f5182-0d6c-4d28-90e1-3eea5d5ea43e",
            "sku_id": "BC34825-30",
            "sku_name": "B/C SHT-N-C RND BULLSEYE TGT 30-8",
            "cost": 18.71,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "61041068-4469-40f9-908e-aa23617f7cee",
            "status": "Unallocated",
            "item_uuid": "e9f1444c-9760-4f26-94b0-4ebc92904771",
            "item_name": "Women’s Ambition S/S",
            "sku_uuid": "9c04fa73-3712-466c-9708-7f8df5123985",
            "sku_id": "NF0A3F17JK3-XL",
            "sku_name": "Women’s Ambition S/S",
            "cost": 65.43,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "d3e503a5-3142-45ca-a678-63a3b0daab64",
        "is_allocated": false,
        "purchase_order_id": "5d606b22-025d-4a20-91db-bb41afc1d74c",
        "created_date": "2018-02-13T23:50:54.859483Z",
        "notes": "Dolorem quod architecto illo earum.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Amy Stewart",
          "business_name": "Frazier-Morrow",
          "address1": "35167 Zachary Estates\nEast Jenna, AK 05465",
          "address2": "78852 Heather Mount Suite 587\nEast Allison, IA 00244-5943",
          "city": "Lake Peterview",
          "state": "Utah",
          "postal_code": "83915",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "b1574c7f-12ac-4f5f-bdac-36aade7cb60f",
            "status": "Unallocated",
            "item_uuid": "a62cbcac-8c9c-45b8-a633-6d63dd4a53f9",
            "item_name": "BH UNIV SNGL POINT SLNG MNT BLK",
            "sku_uuid": "b1baa757-47ab-409a-a70f-c1daa0a1929c",
            "sku_id": "BH70SM04BK",
            "sku_name": "BH UNIV SNGL POINT SLNG MNT BLK",
            "cost": 55.77,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "b0d8075b-080f-43bc-8dc5-f387854e0df7",
            "status": "Unallocated",
            "item_uuid": "d970e287-07b4-4899-9056-425bb7baa1d7",
            "item_name": "FED PD HYDRA-SHK 9MM 135GR 20/200",
            "sku_uuid": "2ff09013-e4b5-4472-92d5-2f4e666a1dbe",
            "sku_id": "FE9HS5PDH",
            "sku_name": "FED PD HYDRA-SHK 9MM 135GR 20/200",
            "cost": 92.59,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "f1e737c3-cbfd-495d-8fc2-b15168b3146e",
            "status": "Unallocated",
            "item_uuid": "c5ea4eb0-7006-4903-8f21-b73ffbe44e05",
            "item_name": "Men’s Short Sleeve Voltage Crew",
            "sku_uuid": "abc1b1ed-eb84-4d2c-a2c6-364bb90c37bc",
            "sku_id": "NF0A353TDYZ-L",
            "sku_name": "Men’s Short Sleeve Voltage Crew",
            "cost": 70.58,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "554d0923-0d44-4cb4-a4b4-a01f5483b462",
            "status": "Unallocated",
            "item_uuid": "6f64fb89-d29a-4f83-acb8-cc6e6a085251",
            "item_name": "Men’s Cyclone 2 Hoodie",
            "sku_uuid": "a5e62f37-264b-49ad-a156-dae541df0836",
            "sku_id": "NF0A2VD91ZQ-XXL",
            "sku_name": "Men’s Cyclone 2 Hoodie",
            "cost": 82.56,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "e2e10547-e398-445d-9e5a-589a08c21bf7",
        "is_allocated": false,
        "purchase_order_id": "3e6b325d-9e05-427f-8a42-4b5a57f21baa",
        "created_date": "2018-02-13T23:50:55.245475Z",
        "notes": "Quae dolor vel dicta natus.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Johnny Avery",
          "business_name": "Mcguire-Jones",
          "address1": "PSC 6302, Box 6679\nAPO AE 20864",
          "address2": "Unit 0825 Box 9332\nDPO AP 92131",
          "city": "New Francisco",
          "state": "Oregon",
          "postal_code": "56157",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "577d61bd-d908-4551-ba8d-3bd1b0b015fd",
            "status": "Unallocated",
            "item_uuid": "d1f98ddd-934e-4e50-bfdf-cc7a28ba888e",
            "item_name": "BTLR CRK FLIP SCOPE COVER 09A EYE",
            "sku_uuid": "15b857c7-0ff2-4f9b-9f42-421624629839",
            "sku_id": "BTLR20095",
            "sku_name": "BTLR CRK FLIP SCOPE COVER 09A EYE",
            "cost": 25.66,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "930355b6-1f5d-4514-833d-14490b7b2240",
            "status": "Unallocated",
            "item_uuid": "befb5fb3-7553-45b7-a867-9b5e06a66b74",
            "item_name": "Minn Kota MKRUS2-8 Humminbird 7 PIn Cable",
            "sku_uuid": "96a98adb-55be-47b6-8c6a-db872407f759",
            "sku_id": "026517",
            "sku_name": "Minn Kota MKRUS2-8 Humminbird 7 PIn Cable",
            "cost": 14.62,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "7287f071-cf11-412b-bd64-d4eebd802063",
            "status": "Unallocated",
            "item_uuid": "bfb3fc1f-2087-47ef-897e-526c61ec3de5",
            "item_name": "Spyderco Police Model Knife Lockback Comboedge",
            "sku_uuid": "965e06cf-3624-4f65-b2cf-bc60c71d8da3",
            "sku_id": "000586",
            "sku_name": "Spyderco Police Model Knife Lockback Comboedge",
            "cost": 94.73,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "953f9a21-aa9d-473d-b675-33699ee3a6d5",
            "status": "Unallocated",
            "item_uuid": "46c27e4e-d270-4611-9612-249bcb368231",
            "item_name": "TRU Ball Velcro Bone Collector Scout Release Black-Large",
            "sku_uuid": "5f05757e-cf2b-4554-b357-c62dc144fad1",
            "sku_id": "1000840",
            "sku_name": "TRU Ball Velcro Bone Collector Scout Release Black-Large",
            "cost": 25.2,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "819b1be1-547a-4142-9cbb-bbca3b4d42a7",
            "status": "Unallocated",
            "item_uuid": "48340d99-4640-44c1-8ace-962f3a47c0d7",
            "item_name": "ADV TECH BUTTSTK/PG MOS/WIN/REM 12GA",
            "sku_uuid": "52c7cfa0-0e52-4bcf-b586-483805265632",
            "sku_id": "ADVSPG0100",
            "sku_name": "ADV TECH BUTTSTK/PG MOS/WIN/REM 12GA",
            "cost": 75.45,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "fd35ba10-b12f-49c6-8ad4-bd01ef5b0ffb",
            "status": "Unallocated",
            "item_uuid": "e1f343d0-b2c6-41d9-8fc7-5e703dec0f9e",
            "item_name": "Women’s Arcata Hoodie",
            "sku_uuid": "b8f05991-9199-45cc-89e3-e39fb52554e8",
            "sku_id": "NF0A3C83L4B-XL",
            "sku_name": "Women’s Arcata Hoodie",
            "cost": 15.23,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "5545ab2f-4ef2-4ea5-aa80-de86732cbcbb",
            "status": "Unallocated",
            "item_uuid": "54529365-41ae-491d-8db5-2292394a0213",
            "item_name": "Women’s Ultra Endurance II",
            "sku_uuid": "7478f90a-f5b0-4d34-bc46-6d96e662a503",
            "sku_id": "NF0A39IF4GH-105",
            "sku_name": "Women’s Ultra Endurance II",
            "cost": 29.87,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "e8107528-1299-4934-aebf-2bdc9752d3b4",
        "is_allocated": false,
        "purchase_order_id": "f577486d-b3c8-4728-8f4c-2c3827a1e01f",
        "created_date": "2018-02-13T23:50:55.834891Z",
        "notes": "Eligendi nostrum consequatur delectus nemo inventore fugit tempora.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Michelle Bruce",
          "business_name": "Lopez Ltd",
          "address1": "7305 Lamb Stravenue Apt. 208\nNew Kenneth, PW 44353-3929",
          "address2": "06539 Thomas Summit\nSouth Debra, WY 93347",
          "city": "Stevenberg",
          "state": "Rhode Island",
          "postal_code": "04943",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "6cb64e1c-bb8e-4323-9251-313edf247618",
            "status": "Unallocated",
            "item_uuid": "164ff3b0-2038-450e-9559-5693cbecb20d",
            "item_name": "Spyderco Tenacious Black G-10 Plainedge",
            "sku_uuid": "ed7fa083-6091-4885-8a32-7b9b9a4fb1b6",
            "sku_id": "008612",
            "sku_name": "Spyderco Tenacious Black G-10 Plainedge",
            "cost": 53.75,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "0993bdce-2d06-4650-9202-46cc7ec5ed56",
            "status": "Unallocated",
            "item_uuid": "3806d768-df7d-4e45-8344-82f2a91c48b3",
            "item_name": "BURRIS HIGH 1\" ZEE RINGS MATTE",
            "sku_uuid": "22efbf76-e108-4f26-b562-399e1ef9ffbc",
            "sku_id": "BU420087",
            "sku_name": "BURRIS HIGH 1\" ZEE RINGS MATTE",
            "cost": 20.94,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "6a198269-2e28-4544-9a20-0f3c73f15e99",
            "status": "Unallocated",
            "item_uuid": "70bec2c3-2581-4940-b1ac-bbafaff70660",
            "item_name": "Hunter Safety  Quick Connect Tree Strap QCS",
            "sku_uuid": "eae16edd-5d35-4045-8b46-0ebf3a07cf79",
            "sku_id": "000250",
            "sku_name": "Hunter Safety  Quick Connect Tree Strap QCS",
            "cost": 32.3,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "5475e12f-0919-440c-b015-4e16e65b66e6",
            "status": "Unallocated",
            "item_uuid": "336c2a3e-f6dd-4487-b7a0-5b5306e23720",
            "item_name": "CORBON DPX 380ACP 80GR BRNS X 20/500",
            "sku_uuid": "baa1c33b-3cb7-4bb8-8cb9-67f23477a330",
            "sku_id": "CORDPX38080",
            "sku_name": "CORBON DPX 380ACP 80GR BRNS X 20/500",
            "cost": 15.44,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "eb9baa7b-d81e-4dbe-8dd0-580cba09ed15",
            "status": "Unallocated",
            "item_uuid": "cb213d10-e1d7-462f-be12-b39fce62dcc7",
            "item_name": "CORBON 45ACP+P 230GR JHP 20/500",
            "sku_uuid": "65d49612-ad21-46e1-b7e3-ccfe4273f2ec",
            "sku_id": "COR45230",
            "sku_name": "CORBON 45ACP+P 230GR JHP 20/500",
            "cost": 66.12,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "a9f5814d-c30b-4199-a6d8-96fdc5959244",
            "status": "Unallocated",
            "item_uuid": "992e4a17-99f4-40b6-9aff-ab9e4effbaa7",
            "item_name": "Men’s Ballard Duck Boot",
            "sku_uuid": "7e18c14e-9c26-4761-93f2-6e98e20571c6",
            "sku_id": "NF00CVX0NGT-090",
            "sku_name": "Men’s Ballard Duck Boot",
            "cost": 90.77,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "e0abf268-3379-45f7-97bf-1ba056f6738a",
            "status": "Unallocated",
            "item_uuid": "615828cb-7a25-4b09-b5ac-7912349591eb",
            "item_name": "Men’s Versitas &#188; Zip",
            "sku_uuid": "972784e1-9eb4-4077-878d-1b01201a37d2",
            "sku_id": "NF0A2V3MJK3-L",
            "sku_name": "Men’s Versitas &#188; Zip",
            "cost": 53.55,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "4fec7086-ba73-46e5-8b51-e4288a1c744b",
            "status": "Unallocated",
            "item_uuid": "0e33da8c-3279-480e-8d0a-6724c7a53ddd",
            "item_name": "Men’s Plaited Crag Crew",
            "sku_uuid": "b8a9d4ab-21ea-45e9-a86c-85edc3b8e075",
            "sku_id": "NF0A3BBDHKW-M",
            "sku_name": "Men’s Plaited Crag Crew",
            "cost": 61.64,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "ac9c05c2-5d8f-46e8-af99-318ab469dff9",
            "status": "Unallocated",
            "item_uuid": "2c02595f-5216-48d0-92b8-404b39e34f48",
            "item_name": "Women’s Nefas Pullover",
            "sku_uuid": "8de16f0e-0462-41f5-b275-29653366cd10",
            "sku_id": "NF0A333SXET-M",
            "sku_name": "Women’s Nefas Pullover",
            "cost": 9.47,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "98a687af-c21a-4e48-90d5-c479755a3309",
            "status": "Unallocated",
            "item_uuid": "b2440e12-b422-4d6d-9a7a-c1a83834762b",
            "item_name": "Men’s Wakerly Hoodie",
            "sku_uuid": "c8056f20-03f3-4052-95c1-9079aad13918",
            "sku_id": "NF0A35DELMW-S",
            "sku_name": "Men’s Wakerly Hoodie",
            "cost": 33.47,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "f30b6bc6-ab70-411f-82bf-0d413c9adcc0",
        "is_allocated": true,
        "purchase_order_id": "1ce39153-a0fc-497c-a398-012fa3ddf48e",
        "created_date": "2018-02-13T23:50:56.625025Z",
        "notes": "Provident vero eum dolores sunt dignissimos nam.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Carl Jones",
          "business_name": "Patrick and Sons",
          "address1": "USNV Hansen\nFPO AP 05781",
          "address2": "013 Rachel Curve Suite 953\nBrandiville, NH 55598-0542",
          "city": "West Melissaburgh",
          "state": "Missouri",
          "postal_code": "67548",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "471bb337-a76c-4ed4-9dc9-e7c5b350b118",
            "status": "HasTracking",
            "item_uuid": "bc533890-986a-4913-b6fa-53dd7f12cc89",
            "item_name": "BTLR CRK FLIP SCOPE COVER 09 OBJ",
            "sku_uuid": "9f172b61-bd03-460a-a203-b2be371e4499",
            "sku_id": "BTLR30090",
            "sku_name": "BTLR CRK FLIP SCOPE COVER 09 OBJ",
            "cost": 29.6,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
            "tracking_numbers": [
              {
                "tracking_number": "G005OI7fsDn1pQSoIbEp5qU7QMmnsxlP",
                "shipping_carrier": "0",
                "shipping_method": "",
                "shipping_weight": "0",
                "shipping_cost": 0,
                "shipping_date": "2018-02-20",
                "quantity": 10
              }
            ],
            "allocation": {
              "quantity_ordered": 10,
              "quantity_allocated": 10,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "02770b69-9bc9-4a0e-b224-414e20ab72da",
            "status": "HasTracking",
            "item_uuid": "e88b9709-5b88-4fc9-8ce8-d19c2dbc9f8c",
            "item_name": "BURRIS XTB SAV S&L FLAT REAR MATTE",
            "sku_uuid": "f4aa688f-9464-44e5-8420-a0c76e5ef5c1",
            "sku_id": "BU410620",
            "sku_name": "BURRIS XTB SAV S&L FLAT REAR MATTE",
            "cost": 51.35,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
            "tracking_numbers": [
              {
                "tracking_number": "G005OI7fsDn1pQSoIbEp5qU7QMmnsxlP",
                "shipping_carrier": "0",
                "shipping_method": "",
                "shipping_weight": "0",
                "shipping_cost": 0,
                "shipping_date": "2018-02-20",
                "quantity": 7
              }
            ],
            "allocation": {
              "quantity_ordered": 7,
              "quantity_allocated": 7,
              "quantity_backordered": 0,
              "quantity_rejected": 0,
              "backorder_date": null
            }
          },
          {
            "uuid": "ae15db3e-2262-473b-9ab2-348c9ad0c617",
            "status": "Unallocated",
            "item_uuid": "d01e29f5-d0e1-409a-a725-2cbfd81554ab",
            "item_name": "BH HIP HLSTR SZ 5 LH BLK",
            "sku_uuid": "895f14de-0a7d-4d4f-a596-0fb059f12317",
            "sku_id": "BH73NH05BK-L",
            "sku_name": "BH HIP HLSTR SZ 5 LH BLK",
            "cost": 76.6,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "8666ecb6-aaa3-43ca-9605-097bdb93f725",
            "status": "Unallocated",
            "item_uuid": "922b0ea4-8989-4792-9071-60ac47a8354b",
            "item_name": "Cannon Dual Rod Holder - Rear Mount 1907070",
            "sku_uuid": "f84cd010-b872-4859-a8f8-758f6384e74e",
            "sku_id": "034987",
            "sku_name": "Cannon Dual Rod Holder - Rear Mount 1907070",
            "cost": 99.74,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "ed02bd4b-dbf3-4b9a-8261-fab02ca56efa",
            "status": "Unallocated",
            "item_uuid": "a1c43f9e-d65e-42ab-bca5-b703d5dd9d7d",
            "item_name": "Frogg Toggs ToadRage Camo Pants Realtree Max 5 HD - Large",
            "sku_uuid": "a153c12b-2e23-4844-8aee-762d78f80267",
            "sku_id": "1002685",
            "sku_name": "Frogg Toggs ToadRage Camo Pants Realtree Max 5 HD - Large",
            "cost": 8.1,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "77d8089a-f2e4-4602-bf4e-4a57238e2241",
            "status": "Unallocated",
            "item_uuid": "42edf126-3bf0-415b-879d-61b0410f0641",
            "item_name": "Girls’ Arctic Swirl Down Jacket",
            "sku_uuid": "7d7a8033-d896-4124-9462-63c6cb3b0754",
            "sku_id": "NF0A34U57D6-XS",
            "sku_name": "Girls’ Arctic Swirl Down Jacket",
            "cost": 56.79,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "b67d9a71-1d5e-46c9-b689-93758256053d",
            "status": "Unallocated",
            "item_uuid": "358cd0bf-41b9-4783-bae1-6c159d86a018",
            "item_name": "Men’s Apex Canyonwall Hybrid Hoodie",
            "sku_uuid": "fe96a8c5-3b6c-4bf0-88a0-2e9b5fd54afe",
            "sku_id": "NF0A3C6VMXW-S",
            "sku_name": "Men’s Apex Canyonwall Hybrid Hoodie",
            "cost": 16.67,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "b25d3749-c179-4cb6-bdda-25120512a745",
            "status": "Unallocated",
            "item_uuid": "d918fa5c-f316-400c-9fcc-5b4ceffcbd8f",
            "item_name": "Women’s Powder Guide Jacket",
            "sku_uuid": "4e834aa8-f393-4ef9-a41c-9cf59a854021",
            "sku_id": "NF0A333EWCE-XL",
            "sku_name": "Women’s Powder Guide Jacket",
            "cost": 45.78,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "d96b1528-3ce6-4a8a-bf0c-a711cf310c0d",
            "status": "Unallocated",
            "item_uuid": "0d6c312d-236a-4fd0-bfca-d818c7732f79",
            "item_name": "Toddler Glacier Full Zip Hoodie",
            "sku_uuid": "58b342a1-cbfc-4f7b-a7c9-d8810ed89cd5",
            "sku_id": "NF0A34WAWXN-2T",
            "sku_name": "Toddler Glacier Full Zip Hoodie",
            "cost": 78.5,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "78d7fdb8-195c-40a2-af3c-b5af17e347b7",
            "status": "Unallocated",
            "item_uuid": "c7cbb514-56af-4ed9-b4f5-7598f0be0518",
            "item_name": "Women’s Strong Is Beautiful High-Rise Pant",
            "sku_uuid": "b27a9ace-bc74-4fa7-91c5-26575556c4c1",
            "sku_id": "NF0A3LMJJK3-L-REG",
            "sku_name": "Women’s Strong Is Beautiful High-Rise Pant",
            "cost": 46.58,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "8665ecd0-ee10-4297-9bf3-7fc94a6add9f",
        "is_allocated": false,
        "purchase_order_id": "97a7ffd0-1f19-41e1-8a6d-7fa964831c72",
        "created_date": "2018-02-13T23:50:57.576497Z",
        "notes": "Dolorem a nesciunt eveniet inventore nesciunt.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Robert Graham",
          "business_name": "Baker, Hinton and Zimmerman",
          "address1": "21158 Reed Extensions Apt. 746\nMarkmouth, CO 85758-0638",
          "address2": "52674 Hoover River Suite 981\nStephenport, ND 53233",
          "city": "Rossfurt",
          "state": "North Dakota",
          "postal_code": "97216",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "f96fcffc-27aa-4c8f-86eb-d3fb50c941ce",
            "status": "Unallocated",
            "item_uuid": "6779b4f0-3ab9-48f6-9823-490de4f8f74c",
            "item_name": "BTLR CRK FLIP SCOPE COVER 23 OBJ",
            "sku_uuid": "f27f08c4-c89c-4b72-b41b-ca2ef2a6c1da",
            "sku_id": "BTLR30230",
            "sku_name": "BTLR CRK FLIP SCOPE COVER 23 OBJ",
            "cost": 65.94,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "610bb8ff-a84e-47bc-b228-3f4634d40411",
            "status": "Unallocated",
            "item_uuid": "77b81d7c-d204-4024-bf1f-46dd47be15e7",
            "item_name": "BH SERPA SPRTSTR FOR GLK19 RH GRY",
            "sku_uuid": "587a84c0-f2e2-452b-b0e7-5a23e3afb089",
            "sku_id": "BH413502BK-R",
            "sku_name": "BH SERPA SPRTSTR FOR GLK19 RH GRY",
            "cost": 93.76,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "a54ffcde-8b81-4641-94af-ca0f38e8f2b5",
            "status": "Unallocated",
            "item_uuid": "aac5f6a5-5d7a-43ae-b93b-584a098584d3",
            "item_name": "Men’s Summit L3 Proprius PrimaLoft&#174; Hoodie",
            "sku_uuid": "6fb09693-c81f-4a5b-a8c7-a5657d77dbcf",
            "sku_id": "NF0A37QR739-L",
            "sku_name": "Men’s Summit L3 Proprius PrimaLoft&#174; Hoodie",
            "cost": 63.66,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
        "uuid": "7c8bcf96-0ab4-42c3-a6fd-f6a4b28c64df",
        "is_allocated": false,
        "purchase_order_id": "580be6fb-e279-4d91-8bd8-91f50da3d9c5",
        "created_date": "2018-02-13T23:50:57.900263Z",
        "notes": "Assumenda doloremque modi laboriosam.",
        "fees": {
          "estimated_shipping_cost": 0,
          "drop_ship_fee": 0,
          "order_fee": 0
        },
        "retailer": {
          "name": "Crux Retailer",
          "uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
          "user": {
            "name": "Roy Breslawski",
            "email": "rbreslawski@cruxretailer.com"
          }
        },
        "address": {
          "name": "Ryan Anderson",
          "business_name": "Davis-Booth",
          "address1": "09642 Mary Crest Suite 200\nNew Sonya, VI 45157",
          "address2": "153 Herrera Harbor\nJenkinsside, OK 73735",
          "city": "North Nichole",
          "state": "Nevada",
          "postal_code": "24078",
          "phone_number": null
        },
        "requested_shipping": {
          "shipping_carrier": "UPS",
          "shipping_method": "Ground"
        },
        "line_items": [
          {
            "uuid": "7886f990-9649-4798-bb6a-9de074ee16da",
            "status": "Unallocated",
            "item_uuid": "3025dda8-8d66-496e-9116-4ac67152fdc3",
            "item_name": "BTLR CRK RECOIL PAD SLIP-ON SML",
            "sku_uuid": "f3850119-a858-4a96-9e85-d23bafa3f9b1",
            "sku_id": "BTLR50325",
            "sku_name": "BTLR CRK RECOIL PAD SLIP-ON SML",
            "cost": 28.4,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "732bc8ce-774b-4d5c-81ed-29e32a6a26dc",
            "status": "Unallocated",
            "item_uuid": "0fe12a6a-df8e-47eb-b2d7-a24f8514d57e",
            "item_name": "B-SQ UNIV CANTILEVER RIB UP TO 3/8",
            "sku_uuid": "b111d12d-a88c-4cbf-8113-ca9fbedaccc3",
            "sku_id": "BSQ16175",
            "sku_name": "B-SQ UNIV CANTILEVER RIB UP TO 3/8",
            "cost": 31.9,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "45baaec2-30e0-4d63-87af-8d9889142017",
            "status": "Unallocated",
            "item_uuid": "20fe6734-cc40-4a8d-ae91-478a7c494401",
            "item_name": "Spyderco Ladybug Lightweight   LBKS3",
            "sku_uuid": "a8c6a5e7-16e4-4ddb-95d1-b69423a393d2",
            "sku_id": "004546",
            "sku_name": "Spyderco Ladybug Lightweight   LBKS3",
            "cost": 61.16,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "5ab7c94a-005b-4aac-8eda-c48590efc42e",
            "status": "Unallocated",
            "item_uuid": "1cd2fdfe-187d-4446-9dde-05499a390c7f",
            "item_name": "QAD Ultra Rest Pro Series LD Black Lefthand",
            "sku_uuid": "ad5ff900-51e1-47e3-9ac6-6f995e4d6ebd",
            "sku_id": "035087",
            "sku_name": "QAD Ultra Rest Pro Series LD Black Lefthand",
            "cost": 27.43,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "671ca6ba-eb11-4f64-84ae-c406b303f981",
            "status": "Unallocated",
            "item_uuid": "37c7ff03-a1ca-4227-9ef0-954051153fd2",
            "item_name": "BERETTA BTM/SIDE ACC RAIL POLY STORM",
            "sku_uuid": "0bcc6e9b-32ef-4b7a-8092-b9a3e1dcefe8",
            "sku_id": "BRE00270",
            "sku_name": "BERETTA BTM/SIDE ACC RAIL POLY STORM",
            "cost": 7.63,
            "supplier_uuid": "757ce28d-fbd6-4b9f-8051-f847482e169f",
            "supplier_name": "Crux Supplier A",
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
            "uuid": "02dec2ad-d677-4d09-be01-a12d171b9d10",
            "status": "Unallocated",
            "item_uuid": "debb92d2-4e51-4a5e-81d6-f022881aa322",
            "item_name": "Men’s Ambition Dual Short",
            "sku_uuid": "8e71439e-744b-4bae-82f7-3c54bbd5c219",
            "sku_id": "NF0A3CEE3EW-L-LNG",
            "sku_name": "Men’s Ambition Dual Short",
            "cost": 5.62,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "fc64c75f-7fb3-4bb7-8b8a-a15c38e3ef3b",
            "status": "Unallocated",
            "item_uuid": "98066829-6240-4c87-b8da-13146e7c8bd5",
            "item_name": "Women’s Climb On Tee",
            "sku_uuid": "837b6eae-55c8-432c-995e-d1f8f982d574",
            "sku_id": "NF0A359TZDN-L",
            "sku_name": "Women’s Climb On Tee",
            "cost": 15.3,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
            "uuid": "47e89bbd-fd40-4504-bf49-9cd78b75dd01",
            "status": "Unallocated",
            "item_uuid": "c8dd53bb-63a0-457d-a184-947e3f29434f",
            "item_name": "Men’s Litewave Fastpack (Graphic)",
            "sku_uuid": "5852b744-5f16-49c7-969d-f4f138784b44",
            "sku_id": "NF0A3FX6THZ-125",
            "sku_name": "Men’s Litewave Fastpack (Graphic)",
            "cost": 71.81,
            "supplier_uuid": "fa18d9a6-1d83-45e0-bebe-41098b0e3925",
            "supplier_name": "ES Docker Cluster Inc",
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
      }
    ]
  }
  ~~~
  {: title="Response" }

---
Get Orders matching certain criteria for your organization. This may contain any or all of your orders: completed, incomplete, processing, etc.


### Request Parameters:

#### Optional:

start
: (int) The Start is the number of which "Order" you would like to start. If no other filters are used, the default order, which is date created, is used. The default Start value is 0. If this filter is not included in your request, the default value is used.

limit
: (int) The Limit is the element number of "Order" in your Orders List where you would like your results to end. If you have 10 orders and you limit at 8 and start at 4, only orders 4, 5, 6, 7, and 8 are included in the results.

line_item_statuses
: (array) One or more line item statuses. Will include orders with statuses based upon that `status_conjunction`. Possible Values are: `Unallocated`, `Allocated`, `Rejected`, `HasTracking`, `Backordered`, `Cancelled`. The response will contain orders with statuses that match the provided line_item_status (as combined based on line_item_status_conjunction).

line_item_status_conjunction
: (string) Determines whether search for line_item_statuses returns orders with a union, intersection, or complement of statuses. Possible values: `and`, `or`, `only`. Default: `or`. The conjunction determines whether we return every order that contains all (and), at least one (or), or only (only) the provided line-item-status(es). For conjunction only, line_item_statuses must have exactly one line-item-status.

start_date
: (string) The Start Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

end_date
: (string) The End Date for your search results. The date must be written in the following format "YYYY-MM-DDThh:mm:ss.000Z"

term
: (string) Term varies depending on if the Orders are for a Retailer or Suppler:
1. For Retailers: term can be either a Record UUID or PO Number.  
2. For Suppliers: term can be either an Order UUID or SKU ID

org_uuids
: (array) An array of Organization Universal Unique Identifiers

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

phone_number
: (number) The Phone Number associated with the address

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

status
: (string) The Status for the Line Item. Possible Values are: `Unallocated`, `Allocated`, `Rejected`, `HasTracking`, `Backordered`, `Cancelled`

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
: (int) The Quantity Ordered of the SKU

quantity_allocated
: (int) The Quantity Allocated by the Supplier for this Order

quantity_backordered
: (int) The Quantity Backordered is the quantity of the order that cannot be shipped because it is currently in a "backordered" state. If you allow the supplier to fulfill the order, this number is supposed to decrease to 0 as they get the item in-stock in their warehouse(s). When a Supplier gets a Backorder Date, they add it to the field labeled "backorder_date".

quantity_rejected
: (int) The Quantity Rejected by the Supplier is the Quantity that they simply cannot fulfill. Reasons may vary, such as state or federal law, customs, or being out-of-stock on an already discontinued product line.

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
curl -X "POST" "https://api-sandbox.cruxconnect.com/orders/" \
     -H 'Authorization: Token dc2ee4bc1b4a87834db8549c0c08fe67e9aabe5d' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "line_item_status_conjunction": "or",
  "start": 0,
  "start_date": "2017-07-31T06:00:00.000Z",
  "limit": 25,
  "line_item_statuses": [
    "unallocated"
  ],
  "end_date": "2018-08-03T06:00:00.000Z",
  "org_uuids": [],
  "term": ""
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/orders/' \
    'Authorization':'Token dc2ee4bc1b4a87834db8549c0c08fe67e9aabe5d' \
    'Content-Type':'application/json; charset=utf-8' \
    line_item_status_conjunction="or" \
    start:=0 \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=25 \
    line_item_statuses:="[
  \"unallocated\"
]" \
    end_date="2018-08-03T06:00:00.000Z" \
    org_uuids:="[]" \
    term=""

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Orders
    # POST https://api-sandbox.cruxconnect.com/orders/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/orders/",
            headers={
                "Authorization": "Token dc2ee4bc1b4a87834db8549c0c08fe67e9aabe5d",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    line_item_status_conjunction="or" \
    start:=0 \
    start_date="2017-07-31T06:00:00.000Z" \
    limit:=25 \
    line_item_statuses:="[
  \"unallocated\"
]" \
    end_date="2018-08-03T06:00:00.000Z" \
    org_uuids:="[]" \
    term="")
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
// request Get Orders 
(function(callback) {
    'use strict';
        
    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/orders/',
        method: 'POST',
        headers: {"Authorization":"Token dc2ee4bc1b4a87834db8549c0c08fe67e9aabe5d","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"start\":0,\"limit\":25,\"line_item_statuses\":[\"unallocated\"],\"line_item_status_conjunction\":\"or\",\"start_date\":\"2017-07-31T06:00:00.000Z\",\"end_date\":\"2018-08-03T06:00:00.000Z\",\"term\":\"\",\"org_uuids\":[]}")
    request.end();
    

})((error, statusCode, headers, body) => {
    console.log('ERROR:', error); 
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
