---
title: /api/organizations/users/all/
name: Get All Users
position: 0.4
type: get
description: Get all users, with user details, specific to your account
right_code: |
  ~~~ json
  {
    "username": "jweir@projectthanos.com",
    "password": "thanosrocks"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  [
    {
      "uuid": "5de38a8e-800e-4cba-84c5-ee6c27f304d8",
      "person": {
        "uuid": "47dffcd8-d237-4d49-a822-e8239b6c2540",
        "first_name": "",
        "last_name": "",
        "email": "dchadwick@projectthanos.com",
        "phone": "+48(5)4653460268"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "5de38a8e-800e-4cba-84c5-ee6c27f304d8"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "0cf5143e-1dd0-4142-b849-bb4048b2b616",
      "person": {
        "uuid": "f983ab24-8d62-4924-b836-93af560ffa23",
        "first_name": "",
        "last_name": "",
        "email": "djones@projectthanos.com",
        "phone": "818-236-6866"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "0cf5143e-1dd0-4142-b849-bb4048b2b616"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "1f6058e3-ea58-4854-b139-1c6980535d4a",
      "person": {
        "uuid": "7ec414df-3e6c-4e7c-abfb-8bb702b50d8e",
        "first_name": "",
        "last_name": "",
        "email": "ejeter@projectthanos.com",
        "phone": "1-115-633-1244"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "1f6058e3-ea58-4854-b139-1c6980535d4a"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "cee37ec7-3e27-4fd9-af47-3b1be2b4e4cc",
      "person": {
        "uuid": "56ec2c2b-94ab-40ce-aa9c-88dc3a309edc",
        "first_name": "",
        "last_name": "",
        "email": "jfischer@projectthanos.com",
        "phone": "097.487.5508"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "cee37ec7-3e27-4fd9-af47-3b1be2b4e4cc"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "e97e2ee3-5f13-40d2-89ed-91e97d09f20c",
      "person": {
        "uuid": "7a7b9cf1-050c-471e-b8e1-749ddcd29418",
        "first_name": "",
        "last_name": "",
        "email": "jtprince@projectthanos.com",
        "phone": "648-172-4252x49570"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "e97e2ee3-5f13-40d2-89ed-91e97d09f20c"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49",
      "person": {
        "uuid": "2e0ecb7e-9426-4e66-a8a9-e69cd8c806c0",
        "first_name": "Jason ",
        "last_name": "Weir",
        "email": "jweir@projectthanos.com",
        "phone": "1-722-036-2568x9442"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "3a7acb28-ab13-437e-8c35-46cf4f0bea49"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "6e1a1a80-78aa-42b0-aa24-4200c0893730",
      "person": {
        "uuid": "ffef3e56-f648-469a-a54f-cff8daa1c96c",
        "first_name": "",
        "last_name": "",
        "email": "kpalmer@projectthanos.com",
        "phone": "871.678.6717"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "6e1a1a80-78aa-42b0-aa24-4200c0893730"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "cefc9200-91eb-40dd-8937-d8edaa8f955f",
      "person": {
        "uuid": "2de10d50-c595-48c3-8cb2-029afd221637",
        "first_name": "",
        "last_name": "",
        "email": "mrbailey@projectthanos.com",
        "phone": "(617)395-2696"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "cefc9200-91eb-40dd-8937-d8edaa8f955f"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "6b7eda16-5e7d-418d-9f52-d129f79add81",
      "person": {
        "uuid": "5fdd4e20-d714-4085-b2bc-796ebc278230",
        "first_name": "",
        "last_name": "",
        "email": "mvijayakumar@projectthanos.com",
        "phone": "493-003-9322"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "6b7eda16-5e7d-418d-9f52-d129f79add81"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "97564794-8a65-4d16-b272-a39973bab31a",
      "person": {
        "uuid": "d55c71ee-44c5-48f4-8dca-7b61fbf6abb7",
        "first_name": "",
        "last_name": "",
        "email": "sallen@projectthanos.com",
        "phone": "257-649-4066x2195"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "97564794-8a65-4d16-b272-a39973bab31a"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "520595e7-7f2a-4ed8-8166-d105b9e74467",
      "person": {
        "uuid": "2580cd88-7b5f-42c2-8b27-df303ce46913",
        "first_name": "",
        "last_name": "",
        "email": "ncoleman@projectthanos.com",
        "phone": "(846)792-3055"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "520595e7-7f2a-4ed8-8166-d105b9e74467"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "889d436c-5a1d-43cb-9d2a-c03254eaea58",
      "person": {
        "uuid": "246e7589-d3d6-4e66-984e-2e7c6c71ab2f",
        "first_name": "",
        "last_name": "",
        "email": "rbreslawski@projectthanos.com",
        "phone": "(403)589-7332x013"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "889d436c-5a1d-43cb-9d2a-c03254eaea58"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "f212167c-36cd-4682-a781-af2df3801db3",
      "person": {
        "uuid": "cd8bf404-87a7-49c3-8e04-72e4da5dee0d",
        "first_name": "",
        "last_name": "",
        "email": "ataylor@projectthanos.com",
        "phone": "871-734-5279"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": false,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "f212167c-36cd-4682-a781-af2df3801db3"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "b10cf41a-cb98-466d-b567-30525d28d28e",
      "person": {
        "uuid": "81505012-fb87-41b5-ba74-8663930675fa",
        "first_name": "",
        "last_name": "",
        "email": "dreschke@projectthanos.com",
        "phone": "1-724-412-9629x77200"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "b10cf41a-cb98-466d-b567-30525d28d28e"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "f9e09488-9e27-4544-8b57-f47995ceb5d7",
      "person": {
        "uuid": "9e762dca-7dab-41ad-afcb-b5b2b1c1930b",
        "first_name": "",
        "last_name": "",
        "email": "ncottle@projectthanos.com",
        "phone": "(979)668-5863x3379"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "f9e09488-9e27-4544-8b57-f47995ceb5d7"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "ac4437a5-a33f-4f0a-9f94-539e950ad9e4",
      "person": {
        "uuid": "09f408d6-365a-47ee-93ad-4f6207235c5c",
        "first_name": "",
        "last_name": "",
        "email": "dmoore@projectthanos.com",
        "phone": "829.425.4479x383"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "ac4437a5-a33f-4f0a-9f94-539e950ad9e4"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "e3921b0a-94ee-4938-97bb-e780aacd971e",
      "person": {
        "uuid": "cb74f29c-8f17-45f5-9559-81ac382068be",
        "first_name": "",
        "last_name": "",
        "email": "dschultz@projectthanos.com",
        "phone": "907.021.0183"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "e3921b0a-94ee-4938-97bb-e780aacd971e"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "440a7219-44f0-4680-896e-70db4d4f87f0",
      "person": {
        "uuid": "48cca101-bc7a-482d-a945-d3ac53e82550",
        "first_name": "",
        "last_name": "",
        "email": "svallen@projectthanos.com",
        "phone": "307.327.7239"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "440a7219-44f0-4680-896e-70db4d4f87f0"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "c9995d6c-da14-43d0-9ec4-a6d2438e4a2b",
      "person": {
        "uuid": "69b41736-ede1-40ba-8460-45a8aa007a7d",
        "first_name": "",
        "last_name": "",
        "email": "kweaver@projectthanos.com",
        "phone": "05977437101"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "c9995d6c-da14-43d0-9ec4-a6d2438e4a2b"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "ba3bcb2b-8be2-4d87-867a-3567746f5261",
      "person": {
        "uuid": "d2aa4a11-5d71-496d-926a-693177f939ae",
        "first_name": "",
        "last_name": "",
        "email": "dmorgan@projectthanos.com",
        "phone": "(517)462-2308"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "ba3bcb2b-8be2-4d87-867a-3567746f5261"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "b821456c-460c-4870-b80b-79017051acf5",
      "person": {
        "uuid": "cfcedf9a-7bbd-4658-9001-7bd8bef5a693",
        "first_name": "owner",
        "last_name": "user",
        "email": "owneruser@projectthanos.com",
        "phone": "240.686.3647x47142"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": false,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "b821456c-460c-4870-b80b-79017051acf5"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "7fce9558-b49a-4a90-b49a-2a38dcb29b23",
      "person": {
        "uuid": "2a3931a6-1c2d-443c-83b6-628b92cc1503",
        "first_name": "Brenda",
        "last_name": "Gillespie",
        "email": "ashleyperry@allen.com",
        "phone": "(797)659-8041"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "7fce9558-b49a-4a90-b49a-2a38dcb29b23"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "817979d4-9d67-4675-a9db-73ac99d9eec7",
      "person": {
        "uuid": "6baf482d-a380-4084-a439-a67b8752f63c",
        "first_name": "Jennifer",
        "last_name": "Garrett",
        "email": "uking@clark-davis.info",
        "phone": "01443719956"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "817979d4-9d67-4675-a9db-73ac99d9eec7"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "2e94381c-6bab-44c0-8d4b-a28f63c56e80",
      "person": {
        "uuid": "5a923565-695b-4dff-be48-07a5225789d4",
        "first_name": "Jennifer",
        "last_name": "Jones",
        "email": "lrobbins@hotmail.com",
        "phone": "01363026237"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "2e94381c-6bab-44c0-8d4b-a28f63c56e80"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "41c6a315-d757-4083-a7a6-82c85e4eae81",
      "person": {
        "uuid": "7f9a3cd2-8015-41a9-a932-d6872bf73afb",
        "first_name": "Regina",
        "last_name": "Cook",
        "email": "markhaas@gmail.com",
        "phone": "(001)542-0239x7459"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "41c6a315-d757-4083-a7a6-82c85e4eae81"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "7871104f-b836-4383-b569-267b07c74a2b",
      "person": {
        "uuid": "38f14a11-ac6a-493f-8e0b-8346b346c1de",
        "first_name": "Maria",
        "last_name": "Williams",
        "email": "matthew99@gmail.com",
        "phone": "1-399-154-8341"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "7871104f-b836-4383-b569-267b07c74a2b"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "fc984b0b-02c0-4cdd-bdc7-27601a2a4fb3",
      "person": {
        "uuid": "57f8a1ad-8f98-4ef1-86f3-8f80f7870c94",
        "first_name": "Kelsey",
        "last_name": "Osborn",
        "email": "kmcbride@hotmail.com",
        "phone": "627.222.6193"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "fc984b0b-02c0-4cdd-bdc7-27601a2a4fb3"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "6e4b513f-5387-42f4-a7c2-571d4e29fb05",
      "person": {
        "uuid": "862d960c-da20-4bfd-a93a-4b2392bf0c81",
        "first_name": "Breanna",
        "last_name": "Fisher",
        "email": "alvaradoscott@gmail.com",
        "phone": "485-189-9017x5890"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "6e4b513f-5387-42f4-a7c2-571d4e29fb05"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "1fd5dcfc-5e61-4621-8844-583ae46c6388",
      "person": {
        "uuid": "b5d6d5a3-a708-4ad5-a1f0-79973352d5e6",
        "first_name": "Sheila",
        "last_name": "Martin",
        "email": "dominique59@newton-santana.org",
        "phone": "(734)600-7685"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "1fd5dcfc-5e61-4621-8844-583ae46c6388"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "5e50b269-1aa8-46c5-9244-a6980b72d0e5",
      "person": {
        "uuid": "82480f25-a531-4e0f-b8eb-caaee42d3e39",
        "first_name": "Kimberly",
        "last_name": "James",
        "email": "hernandezmichael@mann-hunter.biz",
        "phone": "536.461.2834"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "5e50b269-1aa8-46c5-9244-a6980b72d0e5"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "98930d2b-3e85-4d8c-a599-f3db2bbe8494",
      "person": {
        "uuid": "edf6faeb-af2b-438a-9f71-7adc40dce9f3",
        "first_name": "Michael",
        "last_name": "Day",
        "email": "stephen32@gmail.com",
        "phone": "(553)816-5382"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "98930d2b-3e85-4d8c-a599-f3db2bbe8494"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "3ec83d8d-2489-49d7-8cf9-ea743532750d",
      "person": {
        "uuid": "b90b0c83-766d-41fe-bcd2-439e14e9b503",
        "first_name": "Anthony",
        "last_name": "Patterson",
        "email": "alexandria42@gmail.com",
        "phone": "+50(3)7965436200"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "3ec83d8d-2489-49d7-8cf9-ea743532750d"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "a29097ef-9b76-435c-98b7-c39abc3bce71",
      "person": {
        "uuid": "0cfaed72-6264-4bbe-835a-0a7b9b1c1f38",
        "first_name": "Nicholas",
        "last_name": "Flores",
        "email": "bergnatasha@yahoo.com",
        "phone": "807.208.6076"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "a29097ef-9b76-435c-98b7-c39abc3bce71"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "bde8f8df-12a2-4f10-bb83-48cd1e544bfa",
      "person": {
        "uuid": "0631cd3e-edf8-46bb-9f43-5f24fa978907",
        "first_name": "William",
        "last_name": "Sutton",
        "email": "itran@stone.net",
        "phone": "07790154303"
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": true,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": true,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "bde8f8df-12a2-4f10-bb83-48cd1e544bfa"
        }
      },
      "status": "ACTIVE"
    },
    {
      "uuid": "9ea37d85-cdfd-4ee3-904b-bb98454c0ec6",
      "person": {
        "uuid": "b22780a5-645e-44ba-9997-d9258971d1ca",
        "first_name": "–",
        "last_name": "–",
        "email": "asdf@asdf.as",
        "phone": null
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": false,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "9ea37d85-cdfd-4ee3-904b-bb98454c0ec6"
        }
      },
      "status": "CONFIRMATION_WAITING"
    },
    {
      "uuid": "e517fb38-e5e7-4949-b80c-ea420c0dbdd1",
      "person": {
        "uuid": "351c22f3-d2ca-43fc-945f-74d61707d691",
        "first_name": "–",
        "last_name": "–",
        "email": "a@x.com",
        "phone": null
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": false,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "e517fb38-e5e7-4949-b80c-ea420c0dbdd1"
        }
      },
      "status": "CONFIRMATION_WAITING"
    },
    {
      "uuid": "3b45c322-4739-4389-b8a1-9630b3db6ced",
      "person": {
        "uuid": "18aaf56d-61b2-4f99-89d1-82560c40e69b",
        "first_name": "–",
        "last_name": "–",
        "email": "asdf@asf.asdf",
        "phone": null
      },
      "permission_assignments": {
        "permissions": [
          {
            "assigned": false,
            "permission": {
              "uuid": "51690784-8e22-44f2-a6b6-ae3fdb556051",
              "name": "create_org",
              "display_name": "Create Organization",
              "description": "Ability to create an org"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f3854a65-cb5c-4ea6-a0b6-e352328f3f92",
              "name": "update_org_status",
              "display_name": "Update Org Status",
              "description": "Update the org status pending, active, or deactive"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "d3826e60-0f8d-4ca5-b89c-2d2022ece698",
              "name": "create_relationships",
              "display_name": "Create Relationship",
              "description": "Add a relationship between organizaitons, such as supplier to retailer"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "b27056e5-6b4d-409d-aae2-e864019272ea",
              "name": "update_relationship_status",
              "display_name": "Update Relationship Status",
              "description": "Updates the direct relationship status"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "94c61147-51df-4313-b461-82e879392ff3",
              "name": "upload_feed_file",
              "display_name": "Upload Feed file",
              "description": "Uploads the feed file for processing"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "ccd415a0-b72d-4f9e-8a3d-aa2fd2b327ed",
              "name": "view_org_users",
              "display_name": "View Users",
              "description": "Ability to see the users in an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "96501d33-b805-418a-b185-267279876ff3",
              "name": "edit_org_users",
              "display_name": "Edit Users",
              "description": "Ability to edit/change/delete users in an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "75e8c0d1-73cb-4d12-9470-b8e14c0a4731",
              "name": "view_relationships",
              "display_name": "View Relationships",
              "description": "View the direct relationships for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "74208bdf-10bf-4b85-8917-ccf588e1a3ef",
              "name": "view_api_key",
              "display_name": "View API Key",
              "description": "View API keys for the organization, access from other applications"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "422afae9-ba14-4776-9a4d-3b751434b926",
              "name": "create_api_key",
              "display_name": "Create API Key",
              "description": "Creates an API key for the organization, giving access for another application"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f814f6f3-47b5-4cd4-991e-c56858021217",
              "name": "view_org_subscription_plan",
              "display_name": "View Subscription Plan",
              "description": "View the subscription plan info for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "2a0295b6-dd74-4239-9988-24fcdb1adcea",
              "name": "edit_org_subscription_plan",
              "display_name": "Edit Subscription Plan",
              "description": "Edit the subscription plan info for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "05a46c58-9d13-4912-9167-7effc2cc7482",
              "name": "view_payment_info",
              "display_name": "View Payment Info",
              "description": "View the payment information for an organization"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "fa38b242-7db6-4aff-a102-d8b953b22251",
              "name": "edit_payment_info",
              "display_name": "Edit Payment Info",
              "description": "Edit the payment information an org has on file"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "aee4ffa0-fdfb-419b-ac47-8e2cae09b92b",
              "name": "view_billing_statement",
              "display_name": "View Billing Statement",
              "description": "View any billing statements for the org"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "de64f430-03ba-4b92-b071-d0edfdec3e78",
              "name": "view_notifications_settings",
              "display_name": "View Notification Settings",
              "description": "View the notification settings"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "5e5b834d-3cd3-454d-931e-deca06a6159b",
              "name": "edit_email_notifications_preferences",
              "display_name": "Change Notification Settings",
              "description": "Change the email notification prefs"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "327ca720-517f-40d2-97f5-35260d67280b",
              "name": "create_order",
              "display_name": "Create Order",
              "description": "Create an order"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "78b93cfc-4f6d-4838-99b4-b66fbc5ff586",
              "name": "update_order_status",
              "display_name": "Update Order Status",
              "description": "Update an order status"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "89d5b8b0-0c3e-4264-b393-94779ddf7c1d",
              "name": "view_order",
              "display_name": "View Orders",
              "description": "View a single order or list of orders"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4e18f86d-e723-4a49-842d-6924a2427c0a",
              "name": "export_order",
              "display_name": "Export Orders",
              "description": "Export orders"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "44609bde-2afa-4d10-8968-f865c44a4dd1",
              "name": "allocate_order",
              "display_name": "Allocate Order",
              "description": "Update the fullfillment details for an order"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "836db009-d293-46a9-9c2d-9bd56c8cc40b",
              "name": "view_inventory_lists",
              "display_name": "View Inventory Lists",
              "description": "View the inventory lists an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4cd099ef-0537-42ab-a4fc-fff7c77e18fc",
              "name": "edit_inventory_lists",
              "display_name": "Edit Inventory Lists",
              "description": "Edit the inventory lists an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "fedf2d1b-b718-42fd-99f0-25683bb5883e",
              "name": "view_sku_overrides",
              "display_name": "View Sku Overrides",
              "description": "View the sku overrides an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "f0172494-e8bb-4fc4-9546-08f84ff525cd",
              "name": "edit_sku_overrides",
              "display_name": "Edit Sku Overrides",
              "description": "Edit the sku overrides an org has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "8cc10a94-0f58-4113-bda4-2caa63930679",
              "name": "view_supplier_catalogs",
              "display_name": "View Supplier Catalogs",
              "description": "View the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "2699b242-57ce-476d-9076-53b10d67bb78",
              "name": "edit_supplier_catalogs",
              "display_name": "Edit Supplier Catalogs",
              "description": "Edit the supplier catalogs a supplier has created"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "4399a6d6-e64d-4ec2-b43e-ca616737c2e0",
              "name": "view_items",
              "display_name": "View Items",
              "description": "View items from the supplier catalog"
            }
          },
          {
            "assigned": false,
            "permission": {
              "uuid": "6f0c316f-f8cc-4e8b-a4d8-99f99035d0ef",
              "name": "edit_items",
              "display_name": "Edit Items",
              "description": "Edit items from the supplier catalog"
            }
          }
        ],
        "org_user": {
          "uuid": "3b45c322-4739-4389-b8a1-9630b3db6ced"
        }
      },
      "status": "CONFIRMATION_WAITING"
    }
  ]
  ~~~
  {: title="Response" }

---
Get all the details about the users on your account. This displays their name, email, phone number, permissions (roles), and more. Your username and password are optional as you can send your authorization token to receive this information.

URL Endpoint: /api/organizations/users/all/

### Response Parameters:

#### User:

uuid
: (string) Universal Unique Identifier for the User

person
: (object) Person is an object containing a uuid, first name, last name, email, and phone number

permission_assignments
: (object) Permission Assignments is an object containing a list of permissions and an organization User

status
: (string) User's account status which can be "CONFIRMATION WAITING", "ACTIVE", or "DEACTIVATED"

#### Person Object:

uuid
: (string) Universal Unique Identifier for the Person

first_name
: (string) First Name of the Person

last_name
: (string) Last Name of the Person

email
: (string) Email address of the Person

phone
: (string) Phone number of the Person

#### Permission Assignments Object:

permissions
: (list) Permissions are a list of available individual permissions with details as well as if the permission has been assigned to this User

org_user
: (object) Organization User holds the uuid for the User

#### Permissions Object List:

assigned
: (boolean) Assigned indicates whether this particular Permission has been Assigned to this User

permission
: (object) Permission is an object detailing a specific Permission with a uuid, name, display name, and description

#### Permission Object:

uuid
: (string) Universal Unique Identifier for the Permission

name
: (string) Name of the Permission; written in shortened snake case

display_name
: (string) Display Name of the Permission; a more user-friendly name of the Permission

description
: (string) Description of the Permission

| Code | Name                   | Meaning                                                                      |
|------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                     | The API call was received and response is provided                           |
| 400  | Bad Request            | Generally, something required for the request is missing                     |
| 401  | Unauthorized           | Generally, the username or password is incorrect                             |
| 403  | Permission Denied      | Generally, the user does not have permission to perform the requested action |
| 404  | Not Found              | Generally, the call is not sent to the correct URL                           |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                          |


~~~ bash
curl "https://stable.projectthanos.com/api/organizations/users/all/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "username": "jweir@projectthanos.com",
  "password": "thanosrocks"
}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://stable.projectthanos.com/api/organizations/users/all/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'application/json; charset=utf-8' \
    username="jweir@projectthanos.com" \
    password="thanosrocks"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get All Users
    # GET https://stable.projectthanos.com/api/organizations/users/all/

    try:
        response = requests.get(
            url="https://stable.projectthanos.com/api/organizations/users/all/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    username="jweir@projectthanos.com" \
    password="thanosrocks")
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
// request Get All Users
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/organizations/users/all/',
        method: 'GET',
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
    request.write("{\"username\":\"jweir@projectthanos.com\",\"password\":\"thanosrocks\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
