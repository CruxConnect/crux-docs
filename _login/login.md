---
title: /organizations/user-login/
name: Login
position: 0.00
method: post
description: Login to receive an authentication token
right_code: |
  ~~~ json
  {
    "username": "rbreslawski@cruxretailer.com",
    "password": "thanos_rocks"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "auth_token": "dc2ee4bc1b4a87834db8549c0c08fe67e9aabe5d",
    "org_uuid": "93204006-fcdc-458c-8f81-13a7337992ae",
    "user_uuid": "359f4b19-08d1-480b-a6e6-24d5d4e5049d",
    "retailer_uuid": "60148a62-008f-4989-9fd2-f79d13cdc6fb",
    "supplier_uuid": "",
    "org_type": "RETAILER",
    "permission_assignments": {
      "permissions": [
        {
          "assigned": true,
          "permission": {
            "uuid": "68b1647d-b6a7-48b1-9ec2-bf2f1003b6cc",
            "name": "view_org_users",
            "display_name": "View Users",
            "description": "Ability to see the users in an organization",
            "visibility": "BOTH",
            "grouping": "ORGUSERS"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "293d9373-c318-4724-881c-a4e5b0b3e952",
            "name": "edit_org_users",
            "display_name": "Edit Users",
            "description": "Ability to edit/change/delete users in an organization",
            "visibility": "BOTH",
            "grouping": "ORGUSERS"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "83189bd3-fc77-4088-afe8-a35711311037",
            "name": "view_org_subscription_plan",
            "display_name": "View Subscription Plan",
            "description": "View the subscription plan info for an organization",
            "visibility": "BOTH",
            "grouping": "ORGSUB"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "ec83699a-04ed-4fde-bea7-1e96a153bcd6",
            "name": "edit_org_subscription_plan",
            "display_name": "Edit Subscription Plan",
            "description": "Edit the subscription plan info for an organization",
            "visibility": "BOTH",
            "grouping": "ORGSUB"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "27de3480-bed8-45ff-b785-bb5efb363178",
            "name": "view_payment_info",
            "display_name": "View Payment Info",
            "description": "View the payment information for an organization",
            "visibility": "BOTH",
            "grouping": "ORGPAYMENT"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "4bc020fe-4906-4e2e-8663-e5d8e11efe01",
            "name": "edit_payment_info",
            "display_name": "Edit Payment Info",
            "description": "Edit the payment information an org has on file",
            "visibility": "BOTH",
            "grouping": "ORGPAYMENT"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "86977896-d4d8-4b22-92b2-ee3f1db7db1b",
            "name": "view_billing_statement",
            "display_name": "View Billing Statement",
            "description": "View any billing statements for the org",
            "visibility": "BOTH",
            "grouping": "ORGBILLING"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "3fa7ebb3-79d9-4aa4-9fef-f35c49b3ceea",
            "name": "view_notifications_settings",
            "display_name": "View Notification Settings",
            "description": "View the notification settings",
            "visibility": "BOTH",
            "grouping": "ORGNOTIFICATIONS"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "fe492e41-75cf-499c-a399-3f81d1b5ae51",
            "name": "edit_email_notifications_preferences",
            "display_name": "Change Notification Settings",
            "description": "Change the email notification prefs",
            "visibility": "BOTH",
            "grouping": "ORGPAYMENT"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "ab276154-7167-4730-9adf-a22508e4b505",
            "name": "create_order",
            "display_name": "Create Order",
            "description": "Create an order",
            "visibility": "RETAILER",
            "grouping": "ORDERS"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "f4de162c-61e8-49e7-a6a4-f3201c60695e",
            "name": "cancel_order",
            "display_name": "Cancel Order",
            "description": "Cancel an order",
            "visibility": "BOTH",
            "grouping": "ORDERS"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "5188d840-188d-4066-af79-e073a91eb5a3",
            "name": "view_order",
            "display_name": "View Orders",
            "description": "View a single order or list of orders",
            "visibility": "BOTH",
            "grouping": "ORDERS"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "e04aec97-79de-450e-b619-8f909e862495",
            "name": "export_order",
            "display_name": "Export Orders",
            "description": "Export orders",
            "visibility": "BOTH",
            "grouping": "ORDERS"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "a419e4d3-34bd-4894-a794-4de4cc6fb529",
            "name": "view_inventory_lists",
            "display_name": "View Inventory Lists",
            "description": "View the inventory lists an org has created",
            "visibility": "RETAILER",
            "grouping": "PRODINVLIST"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "248b3fdf-c53d-4357-bc5f-52bbae89d3a8",
            "name": "edit_inventory_lists",
            "display_name": "Edit Inventory Lists",
            "description": "Edit the inventory lists an org has created",
            "visibility": "RETAILER",
            "grouping": "PRODINVLIST"
          }
        },
        {
          "assigned": true,
          "permission": {
            "uuid": "58d36a11-cf78-401b-8691-11ae497ee410",
            "name": "view_items",
            "display_name": "View Items",
            "description": "View items from the supplier catalog",
            "visibility": "BOTH",
            "grouping": "PRODITEMS"
          }
        }
      ],
      "org_user": {
        "uuid": "359f4b19-08d1-480b-a6e6-24d5d4e5049d"
      }
    }
  }
  ~~~
  {: title="Response" }

---
Provide a username and password to receive your authentication token and various account-related data. The purpose of the authentication token is to allow you to fetch account-related info without using your username and password. Prior to making other account-related calls, login to get your authentication token.

### Request Parameters:

username
: The username you provided for your Retailer or Supplier account

password
: The password you provided for your Retailer or Supplier account

### Response Parameters:
 
auth_token
: (string) Authentication Token to be used for subsequent API calls

org_uuid
: (string) Organization Universal Unique Identifier for the organization

user_uuid
: (string) User Universal Unique Identifier for the particular user making the API call

retailer_uuid
: (string) Universal Unique Identifier for the Retailer - Only provided if logging into a Retailer Account

supplier_uuid
: (string) Universal Unique Identifier for the Supplier - Only provided if logging into a Supplier Account

org_type
: (string) Defines the type of organization based on credentials

permission_assignments
: (object) Permissions assigned status and Organization User ID

#### Permissions Object

permissions
: (object) Contains two parameters assigned -- a boolean value that that shows if the permission is assigned -- and permission object

##### Permission Object

uuid
: (string) Permission UUID

name
: (string) Permission Name. Permissions include 
- view_org_users 
- edit_org_users
- view_org_subscription_plan
- edit_org_subscription_plan 
- view_payment_info
- edit_payment_info
- view_billing_statement
- view_notifications_settings
- edit_email_notifications_preferences
- create_order
- cancel_order
- view_order
- export_order
- view_inventory_lists
- edit_inventory_lists
- view_items


display_name
: (string) Permission Display Name

description
: (string) Description of the Permission

visibility
: (string) User type with visibility of the permission.  These include 'RETAILER', 'SUPPLIER', or 'BOTH'

grouping
: (string) Permission grouping.  These include 
- ORGUSERS
- ORGSUB
- ORGPAYMENT
- ORGBILLING
- ORGNOTIFICATIONS
- ORDERS

#### Organization User Object

uuid
: (string) User's Organization UUID

Expected responses include 200, 400, 401, 403, or 404.


~~~ bash
curl -X "POST" "https://api-sandbox.cruxconnect.com/organizations/user-login/" \
     -H 'Authorization: ' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "username": "rbreslawski@cruxretailer.com",
  "password": "thanos_rocks"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://api-sandbox.cruxconnect.com/organizations/user-login/' \
    'Authorization':'' \
    'Content-Type':'application/json; charset=utf-8' \
    username="rbreslawski@cruxretailer.com" \
    password="thanos_rocks"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Login
    # POST https://api-sandbox.cruxconnect.com/organizations/user-login/

    try:
        response = requests.post(
            url="https://api-sandbox.cruxconnect.com/organizations/user-login/",
            headers={
                "Authorization": "",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    username="rbreslawski@cruxretailer.com" \
    password="thanos_rocks")
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
// request Login 
(function(callback) {
    'use strict';
        
    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/organizations/user-login/',
        method: 'POST',
        headers: {"Authorization":"","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{\"username\":\"rbreslawski@cruxretailer.com\",\"password\":\"thanos_rocks\"}")
    request.end();
    

})((error, statusCode, headers, body) => {
    console.log('ERROR:', error); 
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
