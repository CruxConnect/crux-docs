---
title: /api/organizations/users/detail/&ltuser_uuid&gt/
name: Get User
position: 0.5
type: get
description: Get all details about a single user on your account
right_code: |
  ~~~ json
  {
    "username": "jweir@projectthanos.com",
    "password": "thanosrocks"
  }
  ~~~
  {: title="Request" }

  ~~~ json
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
  }
  ~~~
  {: title="Response" }

---
Get all the details about a specific user on your Retailer or Supplier account. This displays their name, email, phone number, permissions (roles), and more. Your username and password are optional as you can send your authorization token to receive this information. For this particular call, the user's uuid must be added to the URL endpoint.

URL Endpoint: /api/organizations/users/detail/\<user_uuid\>/

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
: (object list) Permissions are a list of available individual permissions with details as well as if the permission has been assigned to this User

org_user
: (object) Organization User holds the uuid for the User

#### Permissions List Object:

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
curl "https://stable.projectthanos.com/api/organizations/users/detail/3a7acb28-ab13-437e-8c35-46cf4f0bea49/" \
     -H 'Authorization: Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
     -H 'Content-Type: text/plain; charset=utf-8' \
     -d $'{
  "username": "jweir@projectthanos.com",
  "password": "thanosrocks"
}'

~~~
{: title="Curl" }

~~~ bash
http --form GET 'https://stable.projectthanos.com/api/organizations/users/detail/3a7acb28-ab13-437e-8c35-46cf4f0bea49/' \
    'Authorization':'Token a0f17278bed479ee719ea890b8caf0329e1f3e5b' \
    'Content-Type':'text/plain; charset=utf-8' \
    'data'=$'{
  \"username\": \"jweir@projectthanos.com\",
  \"password\": \"thanosrocks\"
}'

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Get User
    # GET https://stable.projectthanos.com/api/organizations/users/detail/3a7acb28-ab13-437e-8c35-46cf4f0bea49/

    try:
        response = requests.get(
            url="https://stable.projectthanos.com/api/organizations/users/detail/3a7acb28-ab13-437e-8c35-46cf4f0bea49/",
            headers={
                "Authorization": "Token a0f17278bed479ee719ea890b8caf0329e1f3e5b",
                "Content-Type": "text/plain; charset=utf-8",
            },
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
// request Get User
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/organizations/users/detail/3a7acb28-ab13-437e-8c35-46cf4f0bea49/',
        method: 'GET',
        headers: {"Authorization":"Token a0f17278bed479ee719ea890b8caf0329e1f3e5b","Content-Type":"text/plain; charset=utf-8"}
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
    request.write("{\n  \"username\": \"jweir@projectthanos.com\",\n  \"password\": \"thanosrocks\"\n}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
