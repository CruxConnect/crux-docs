---
title: Tracking
name:
position: 7
visibility: file-specs
method:
description: Tracking Stuff
right_code: |

---

#### Tracking
_Supplier Fields_

order_uuid
: (string) The Universal Unique Identifier for the Order

tracking_number
: (string) ***Required*** Order tracking number

supplier_provided_carrier
: (string) Supplier provided carrier

supplier_provided_method
: (string) Supplier provided shipping method

package_weight
: (float) Package weight

package_ship_cost
: (float) Package shipping cost

package_ship_date
: (float) Package ship date

line_items
: (object_) ***Required*** An array of line item objects

package_uuid
: (string) Package Universal Unique Identifier


