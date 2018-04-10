---
title: /organizations/connections/request/
name: Get Requested Connection Detail
method: GET
visibility: public
description: Get a list of requested connections
right_code: |
  ~~~ json
  {
    "limit": "40",
    "start": "3"
  }
  ~~~
  {: title="Request" }

  ~~~ json
  {
    "requests": [
      {
        "uuid": 'xxxxxx-xxxx-x-x-x-x-xx',
        "name": "Pudding And Pie LLC",
        "status" "Pending", // Perhaps cancelled/completed?
        "created": "<datetime>",
        "updated": "<datetime>",
        "website": "www.example.com",
        "contact": {
          "uuid": "2e0ecb7e-9426-4e66-a8a9-e69cd8c806c0",
          "name": "Georgie Porgie",
          "email": "gporgie@puddingandpie.com",
          "phone": "1-722-036-2568x9442"
        },
      },
      { ... }
    ]
    "pagination": {...}
  ~~~
  {: title="Response" }
---

### Request Parameters:

limit
: (int) Number of suppliers displayed on a page; used for paginating results. Default: 50. Maximum: 100. Any 'limit' greater than the Maximum will be forced to the Maximum.

start
: (int) Element number of the first supplier that will be displayed on a page. (The available suppliers are returned in an ordered list, numbered from 0 to Number-of-suppliers, with each supplier an element in the list.) Used for paginating results. Default: 0. If greater than or equal to the number of available suppliers, 'start' is forced to the Number-of-suppliers (which will yield zero results).

### Response Parameters:

requests
: (array) A list of connection request objects (see below)

pagination
: (object) The Pagination object parameter includes the total_count, start, and limit for your Search.


#### Connection Request Object:

uuid
: (string) UUID of the connection request

name
: (string) Name of the organization to which the request is to connect

status
: (string) Status of the request (pending/cancelled/completed)

created
: (datetime) Time the request was created

updated
: (datetime) Last time the request was updated

website
: (string) The conectee's website

contact
: (object) The contact information for the connectee


<!-- TODO: turn this block into: {% include objects/contact.md %} -->
##### Contact object

name
: (string) The contact name

phone
: (string) The contact phone

email
: (string) The contact email

<!-- TODO: turn this block into: {% include objects/pagination.md %} -->
#### Pagination Object:

total_count
: (number) The Total Count of results returned for this Search

start
: (number) The Start parameter indicates on which element of the list of results the pagination should begin.

limit
: (number) The Limit parameter indicates one which element of the list of results the pagination should end.
