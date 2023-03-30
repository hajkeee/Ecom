# E-Commerce dataLayer for GA4 and GTM

### Zadanie rekrutacyjne Digital Analyst
  ### Referencje
- [Data Layer](https://developers.google.com/tag-platform/devguides/datalayer?hl=en)
- [GA4 Events](https://developers.google.com/analytics/devguides/collection/ga4/reference/events)
- [GA4 Objects schema](https://support.google.com/analytics/answer/10119380?hl=en)
- [Google E-Commerce example Website](https://enhancedecommerce.appspot.com/)

### GA4 Events (implementation via source code and datalayer)
| Event Name | Explanation | 
| ---------- | ----------- | 
| view_item | Tracking the display of a product |
## gtag Implementation Example:
```html
gtag("event",  "view_item",  {
  "items": [{
    "item_id": "7w9e0",
    "item_name": "Masons T-Shirt",
    "price": "31.00",
    "item_brand": "Masons",
    "item_category": "T-Shirts",
    "index": 0
  }],
  "currency": "USD"
});
```
## DataLayer Implementation Example:
```html 
dataLayer.push({
   "event":  "view_item",
   "ecommerce":  {
    "items": [{
      "item_id": "7w9e0",
      "item_name": "Masons T-Shirt",
      "price": "31.00",
      "item_brand": "Masons",
      "item_category": "T-Shirts",
      "index": 0
    }],
    "currency": "USD"
  }
});
```
##
| Event Name | Explanation | 
| ---------- | ----------- | 
| add_to_cart | Tracking the display of a product |

## gtag Implementation Example:
```html
gtag("event",  "add_to_cart",  {
  "currency": "USD",
  "value": 31,
  "items": [{
    "item_id": "7w9e0",
    "item_name": "Masons T-Shirt",
    "price": "31.00",
    "quantity": 1,
    "item_brand": "Masons",
    "item_category": "T-Shirts",
    "item_variant": "red",
    "index": 0,
    "size": "M"
  }]
});
```
## DataLayer Implementation Example:
```html 
dataLayer.push({
   "event":  "add_to_cart",
   "ecommerce":  {
    "currency": "USD",
    "value": 31,
    "items": [{
      "item_id": "7w9e0",
      "item_name": "Masons T-Shirt",
      "price": "31.00",
      "quantity": 1,
      "item_brand": "Masons",
      "item_category": "T-Shirts",
      "item_variant": "red",
      "index": 0,
      "size": "M"
    }]
  }
});
```

| Event Name | Explanation | 
| ---------- | ----------- | 
| remove_from_cart | Tracking the display of a product |

## gtag Implementation Example:
```html
gtag("event",  "remove_from_cart",  {
  "currency": "USD",
  "value": 31,
  "items": [{
    "item_id": "7w9e0",
    "item_name": "Masons T-Shirt",
    "price": "31.00",
    "quantity": 1,
    "item_brand": "Masons",
    "item_category": "T-Shirts",
    "item_variant": "red",
    "index": 0,
    "size": "M"
  }]
});
```
## DataLayer Implementation Example:
```html 
dataLayer.push({
   "event":  "remove_from_cart",
   "ecommerce":  {
    "currency": "USD",
    "value": 31,
    "items": [{
      "item_id": "7w9e0",
      "item_name": "Masons T-Shirt",
      "price": "31.00",
      "quantity": 1,
      "item_brand": "Masons",
      "item_category": "T-Shirts",
      "item_variant": "red",
      "index": 0,
      "size": "M"
    }]
  }
});
```
