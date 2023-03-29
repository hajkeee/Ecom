# E-Commerce dataLayer for GA4 and GTM

### Zadanie rekrutacyjne Digital Analyst
  ### Referencje
- [Data Layer](https://developers.google.com/tag-platform/devguides/datalayer?hl=en)
- [GA4 Events](https://developers.google.com/analytics/devguides/collection/ga4/reference/events)
- [GA4 Objects schema](https://support.google.com/analytics/answer/10119380?hl=en)
- [Google E-Commerce example Website](https://enhancedecommerce.appspot.com/)

### GA4 Events (implementation via source code)
| Event Name | Explanation | Code Example |
| ---------- | ----------- | ------------ |
| view_item | Tracking the display of a product | `gtag("event", "view_item", {"items":[{"item_id":"9bdd2","item_name":"Compton T-Shirt","price":"44.00","item_brand":"Compton","item_category":"T-Shirts","index":0}],"currency":"USD"}) |
