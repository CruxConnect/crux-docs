### URL

```
POST /products/inventory-lists/<uuid>/item-search/
```

Searches a specific inventory list and returns a few results in the context of
that inventory list.

The request and response are _exactly_ like the standard catalog search
except:

* The inventory list uuid need not be provided as a facet (it will be
  auto-injected).
* Returns `included_sku_count` which is the number of skus found in _that_
  inventory list that are also in the item.
* [There was one more thing]

### Request

Same as the catalog search endpoint.

### Response

Same as catalog search except `included_sku_count` will be added to the item
level output.
