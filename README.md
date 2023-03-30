# E-Commerce dataLayer for GA4 and GTM

### Zadanie rekrutacyjne Digital Analyst
  ### Referenсes 
- [Data Layer](https://developers.google.com/tag-platform/devguides/datalayer?hl=en)
- [GA4 Events](https://developers.google.com/analytics/devguides/collection/ga4/reference/events)
- [GA4 Objects schema](https://support.google.com/analytics/answer/10119380?hl=en)
- [Google E-Commerce example Website](https://enhancedecommerce.appspot.com/)

### GA4 Events (implementation via source code and datalayer)
| Event Name | Explanation | 
| ---------- | ----------- | 
| view_item | To measure how many times item details are viewed, send a view_item event whenever a user views an item’s details screen. |
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
| add_to_cart | To measure when someone adds merchandise to their shopping cart as a conversion, you need to set up the add_to_cart event on your website or app. |

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
| remove_from_cart | To measure when a user removes an item from a cart, send the remove_from_cart event. |

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
| begin_checkout | Measure the first step in a checkout process by sending a begin_checkout event with one or more items defined with the relevant fields. A coupon can also be added at this stage to the entire order by adding it to the event or applied to a particular item by adding it to specific elements in the items array. |

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
| add_shipping_info | When a user proceeds to the next step in the checkout process and adds shipping information, send an add_shipping_info event.  |

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
| add_payment_info | Send the add_payment_info event when a user submits their payment information. If applicable, include payment_type with this event for the chosen method of payment |

## gtag Implementation Example:
```html
gtag("event",  "add_payment_info",  {
  "value": 31,
  "currency": "USD",
  "payment_type": "Credit Card"
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
| Purchase | Measure a purchase by sending a purchase event with one or more items defined with the relevant fields |

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
