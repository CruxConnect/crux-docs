---
title: /timp/organizations/connections/
name: Get Connections
position: 5.04
visibility: public
method: get
description: Get all direct Connections specific to your account
right_code: |
  ~~~ json
  [
    {
      "uuid": "c3081fd8-202b-47f2-9347-63d3c27028f1",
      "retailer": {
        "uuid": "a5daa91c-79e7-4d79-a7b2-04519d6feba1",
        "organization": {
          "uuid": "ebf3657c-2abb-4aff-be70-69082acc9302",
          "name": "projectthanos",
          "website": "projectthanos.com",
          "org_type": "RETAILER",
          "status": "ACTIVE",
          "created_date": "2018-06-28T12:55:17.774287Z",
          "active_date": null,
          "account_manager": {
            "uuid": "80abd247-9cc7-4219-97a9-d74fec7e55d2",
            "person": {
              "uuid": "6f6c0a1d-38ea-445d-a616-c025ffb18a73",
              "first_name": "Joe",
              "last_name": "Account",
              "email": "joe@cruxaccountmanager.com",
              "phone": "07365022005",
              "job_title": "Account Manager"
            }
          },
          "retailer_uuid": "a5daa91c-79e7-4d79-a7b2-04519d6feba1",
          "supplier_uuid": ""
        },
        "contact": {
          "uuid": "9024e5ed-d25b-4a12-b1ac-4f833486a7ee",
          "first_name": "owner",
          "last_name": "user",
          "email": "owneruser7@projectthanos.com",
          "phone": "929-954-4549x827",
          "job_title": "Account Manager"
        }
      },
      "supplier": {
        "uuid": "ed0eb521-1a0a-4526-a155-31daa726e66c",
        "organization": {
          "uuid": "fddc07e7-4383-4e63-929f-f10c3b0864f0",
          "name": "projectzuul",
          "website": "projectzuul.com",
          "org_type": "SUPPLIER",
          "status": "ACTIVE",
          "created_date": "2018-06-28T12:55:20.293262Z",
          "active_date": null,
          "account_manager": null,
          "retailer_uuid": "",
          "supplier_uuid": "ed0eb521-1a0a-4526-a155-31daa726e66c"
        },
        "contact": {
          "uuid": "1098f5e9-a343-4adc-9969-c63a184250db",
          "first_name": "owner",
          "last_name": "user",
          "email": "owneruser8@projectzuul.com",
          "phone": "1-638-579-0251x5182",
          "job_title": "Account Manager"
        }
      },
      "status": "ACTIVE",
      "account_manager": {
        "uuid": "80abd247-9cc7-4219-97a9-d74fec7e55d2",
        "person": {
          "uuid": "6f6c0a1d-38ea-445d-a616-c025ffb18a73",
          "first_name": "Joe",
          "last_name": "Account",
          "email": "joe@cruxaccountmanager.com",
          "phone": "07365022005",
          "job_title": "Account Manager"
        }
      },
      "allocation_type": null,
      "suppliers_retailer_account_number": null,
      "retailers_supplier_account_number": null,
      "deactivated_date": null
    },
    {
      "uuid": "6b062210-6f5f-45bb-bf9a-100574368013",
      "retailer": {
        "uuid": "a5daa91c-79e7-4d79-a7b2-04519d6feba1",
        "organization": {
          "uuid": "ebf3657c-2abb-4aff-be70-69082acc9302",
          "name": "projectthanos",
          "website": "projectthanos.com",
          "org_type": "RETAILER",
          "status": "ACTIVE",
          "created_date": "2018-06-28T12:55:17.774287Z",
          "active_date": null,
          "account_manager": {
            "uuid": "80abd247-9cc7-4219-97a9-d74fec7e55d2",
            "person": {
              "uuid": "6f6c0a1d-38ea-445d-a616-c025ffb18a73",
              "first_name": "Joe",
              "last_name": "Account",
              "email": "joe@cruxaccountmanager.com",
              "phone": "07365022005",
              "job_title": "Account Manager"
            }
          },
          "retailer_uuid": "a5daa91c-79e7-4d79-a7b2-04519d6feba1",
          "supplier_uuid": ""
        },
        "contact": {
          "uuid": "9024e5ed-d25b-4a12-b1ac-4f833486a7ee",
          "first_name": "owner",
          "last_name": "user",
          "email": "owneruser7@projectthanos.com",
          "phone": "929-954-4549x827",
          "job_title": "Account Manager"
        }
      },
      "supplier": {
        "uuid": "904e880a-0f8b-4e25-86ff-e63588914c95",
        "organization": {
          "uuid": "d6ac857d-c844-4312-8485-6d121d065308",
          "name": "Stevens, Smith and Krause",
          "website": "rojas.com",
          "org_type": "SUPPLIER",
          "status": "ACTIVE",
          "created_date": "2018-06-28T12:55:15.811874Z",
          "active_date": null,
          "account_manager": null,
          "retailer_uuid": "",
          "supplier_uuid": "904e880a-0f8b-4e25-86ff-e63588914c95"
        },
        "contact": {
          "uuid": "f1b298cf-c4a3-4a69-a098-5ee2e590512c",
          "first_name": "Natalie",
          "last_name": "Berger",
          "email": "drosales@smith.org",
          "phone": "169-160-4019",
          "job_title": "Account Manager"
        }
      },
      "status": "ACTIVE",
      "account_manager": {
        "uuid": "80abd247-9cc7-4219-97a9-d74fec7e55d2",
        "person": {
          "uuid": "6f6c0a1d-38ea-445d-a616-c025ffb18a73",
          "first_name": "Joe",
          "last_name": "Account",
          "email": "joe@cruxaccountmanager.com",
          "phone": "07365022005",
          "job_title": "Account Manager"
        }
      },
      "allocation_type": null,
      "suppliers_retailer_account_number": null,
      "retailers_supplier_account_number": null,
      "deactivated_date": null
    },
    {
      "uuid": "0db8f846-cd78-4b13-b6b4-3e2880fc7eac",
      "retailer": {
        "uuid": "a5daa91c-79e7-4d79-a7b2-04519d6feba1",
        "organization": {
          "uuid": "ebf3657c-2abb-4aff-be70-69082acc9302",
          "name": "projectthanos",
          "website": "projectthanos.com",
          "org_type": "RETAILER",
          "status": "ACTIVE",
          "created_date": "2018-06-28T12:55:17.774287Z",
          "active_date": null,
          "account_manager": {
            "uuid": "80abd247-9cc7-4219-97a9-d74fec7e55d2",
            "person": {
              "uuid": "6f6c0a1d-38ea-445d-a616-c025ffb18a73",
              "first_name": "Joe",
              "last_name": "Account",
              "email": "joe@cruxaccountmanager.com",
              "phone": "07365022005",
              "job_title": "Account Manager"
            }
          },
          "retailer_uuid": "a5daa91c-79e7-4d79-a7b2-04519d6feba1",
          "supplier_uuid": ""
        },
        "contact": {
          "uuid": "9024e5ed-d25b-4a12-b1ac-4f833486a7ee",
          "first_name": "owner",
          "last_name": "user",
          "email": "owneruser7@projectthanos.com",
          "phone": "929-954-4549x827",
          "job_title": "Account Manager"
        }
      },
      "supplier": {
        "uuid": "14b1afb6-6bbc-47ca-90c4-6a3925aa654c",
        "organization": {
          "uuid": "97248615-43ab-43e9-bd3c-acd59ca642b0",
          "name": "shagster",
          "website": "shagster.com",
          "org_type": "SUPPLIER",
          "status": "PENDING",
          "created_date": "2018-08-07T16:44:41.358121Z",
          "active_date": null,
          "account_manager": {
            "uuid": "80abd247-9cc7-4219-97a9-d74fec7e55d2",
            "person": {
              "uuid": "6f6c0a1d-38ea-445d-a616-c025ffb18a73",
              "first_name": "Joe",
              "last_name": "Account",
              "email": "joe@cruxaccountmanager.com",
              "phone": "07365022005",
              "job_title": "Account Manager"
            }
          },
          "retailer_uuid": "",
          "supplier_uuid": "14b1afb6-6bbc-47ca-90c4-6a3925aa654c"
        },
        "contact": {
          "uuid": "55cc72aa-b6cb-4d21-88eb-3b17f8fafe01",
          "first_name": "shag",
          "last_name": "theshag",
          "email": "shag@shagster.com",
          "phone": null,
          "job_title": null
        }
      },
      "status": "ACTIVE",
      "account_manager": {
        "uuid": "80abd247-9cc7-4219-97a9-d74fec7e55d2",
        "person": {
          "uuid": "6f6c0a1d-38ea-445d-a616-c025ffb18a73",
          "first_name": "Joe",
          "last_name": "Account",
          "email": "joe@cruxaccountmanager.com",
          "phone": "07365022005",
          "job_title": "Account Manager"
        }
      },
      "allocation_type": null,
      "suppliers_retailer_account_number": "",
      "retailers_supplier_account_number": "",
      "deactivated_date": null
    }
  ]
  ~~~
  {: title="Response" }

---
Get all of the direct Connections specific to your account. These Connections show what suppliers and/or retailers are available to you with related information such as account managers and contact information.

### Response Parameters:

uuid
: (string) Universal Unique Identifier for a Connection

retailer
: (object) Retailer object containing a uuid, and an organization object

supplier
: (object) Supplier object containing a uuid, and an organization object

status
: (string) Status for the Connection, which can be "CONFIRMATION WAITING", "ACTIVE", or "DEACTIVATED"

account_manager
: (object) Your assigned account manager

suppliers_retailer_account_number
: (string) Supplier's retailer account number

retailers_supplier_account_number
: (string) Retailer's supplier account number


#### Retailer Object:

uuid
: (string) Universal Unique Identifier for a Retailer

organization
: (object) Organization object containing a uuid, name, organization type, status, created date, active date, and an account manager

contact
: (object) Retailer Contact

#### Supplier:

uuid
: (string) Universal Unique Identifier for the Supplier

organization
: (object) Organization object containing a uuid, name, organization type, status, created date, active date, and an account manager

contact
: (object) Supplier Contact

#### Organization Object:

uuid
: (string) Universal Unique Identifier for an Organization

name
: (string) Name of the Organization

website : (string) Browser-ready URL for supplier's public-facing website. A URL is 'browser-ready' if we can put it in an internet browser and the website loads. (For some websites that means that the protocol needs to be specified, eg, 'https://www.awesome.com'; for others, the protocol is not required, eg, 'www.verycool.com'.)

org_type
: (string) Organization Type defines if the organization is a "RETAILER" or a "SUPPLIER"

status
: (string) Status for the Organization, which can be "PENDING", "ACTIVE", or "DEACTIVATED"

created_date
: (string) Created Date; the Date when the Organization was Created within our system

active_date
: (string) Active Date; the Date when the Organization became Active within our system

account_manager
: (object) Account Manager object containing a uuid and an organization user

#### Contact Object

{% include timp/objects/contact.md %}

#### Account Manager Object:

uuid
: (string) Universal Unique Identifier for an Account Manager

person
: (object) Person is an object containing a uuid, first name, last name, email, and phone number

#### Person Object:

{% include timp/objects/contact.md %}

### Expected Response Codes

{% include timp/links/response_codes.md %}


~~~ bash
curl "https://api-sandbox.cruxconnect.com/timp/organizations/connections/" \
     -H 'Authorization: Token 1234567890' \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{}'

~~~
{: title="Curl" }

~~~ bash
http --json GET 'https://api-sandbox.cruxconnect.com/timp/organizations/connections/' \
    'Authorization':'Token 1234567890' \
    'Content-Type':'application/json; charset=utf-8'


~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Get Connections
    # GET https://api-sandbox.cruxconnect.com/timp/organizations/connections/

    try:
        response = requests.get(
            url="https://api-sandbox.cruxconnect.com/timp/organizations/connections/",
            headers={
                "Authorization": "Token 1234567890",
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps()
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
// request Get Connections
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'api-sandbox.cruxconnect.com',
        port: '443',
        path: '/timp/organizations/connections/',
        method: 'GET',
        headers: {"Authorization":"Token 1234567890","Content-Type":"application/json; charset=utf-8"}
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
    request.write("{}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }
