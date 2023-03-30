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
| Event Name | Explanation | 
| ---------- | ----------- | 
| begin_checkout | Tracking the display of a product |

## gtag Implementation Example:
```html
gtag("event",  "begin_checkout",  {
  "value": 31,
  "currency": "USD",
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
   "event":  "begin_checkout",
   "ecommerce":  {
    "value": 31,
    "currency": "USD",
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
| add_shipping_info | Tracking the display of a product |

## gtag Implementation Example:
```html
gtag("event",  "add_shipping_info",  {
  "value": 31,
  "currency": "USD",
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
   "event":  "add_shipping_info",
   "ecommerce":  {
    "value": 31,
    "currency": "USD",
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
| add_payment_info | Tracking the display of a product |

## gtag Implementation Example:
```html
gtag("event",  "add_payment_info",  {
  "value": 31,
  "currency": "USD",
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
   "event":  "add_payment_info",
   "ecommerce":  {
    "value": 31,
    "currency": "USD",
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
| add_payment_info | Tracking the display of a product |

## gtag Implementation Example:
```html
gtag("event",  "purchase",  {
  "transaction_id": "84b49088-1c34-4a6b-8d85-28f0f3b6a7e9",
  "currency": "USD",
  "tax": 5,
  "shipping": 5,
  "value": 41,
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
   "event":  "purchase",
   "ecommerce":  {
    "transaction_id": "84b49088-1c34-4a6b-8d85-28f0f3b6a7e9",
    "currency": "USD",
    "tax": 5,
    "shipping": 5,
    "value": 41,
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
