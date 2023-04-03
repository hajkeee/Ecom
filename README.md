# E-Commerce dataLayer for GA4. Measurement Plan

  ### Introduction
   Thank you for providing me with this task. I must say that the current setup is quite extensive, and it was a bit challenging for me to identify any gaps or areas      of improvement within the current GA4/GA3 implementation. It's difficult to imagine that nothing has been implemented on the website at this point. Essentially, it    seems that everything I will discuss in this document has already been covered.
    
   I want to emphasize that for the past two years, my work has mainly been focused on tagging. While I will do my best to provide insights from an analytics              perspective, I want to acknowledge that my perspective may be limited.
  
  
  ### Identify the business objectives
   In this paragraph, I would like to explain my perspective on e-commerce websites. First and foremost, such websites should generate profit. From my point of view,      this is the key indicator of success. 
   
   To be successful in e-commerce business, it is important to utilize popular advertising platforms such as Google Ads (since I am more familiar with Google, I will      only mention this platform).
   
   Unfortunately, even with well-targeted ads and large budgets, advertising may not produce the desired results. In my opinion, for a website to generate profit and      for advertising to work effectively for a business, the following aspects need to be understood and considered:
   
   1. Website convenience, speed of loading, and optimization. Regarding this point, I would like to make a small note. Specifically, on my device with a powerful           graphics card and processor, stable internet connection, the website loaded quite slowly, and the CPU load increased several times. I'm not sure what could be         causing this, possibly my location, but I still wanted to point out this issue.
   2. Website customer support and navigation. In this point, it is important to understand that even if a business offers the cheapest/most affordable products, the         reputation of the website is crucial. If all users complain about the difficult return process, hidden fees, slow customer support, then even with perfectly           targeted advertising, users may avoid doing business with this company.
   3. A good UI and an easy-to-understand purchasing process are crucial for the success of any e-commerce website. Based on my personal experience, I have often             encountered issues with poorly designed user interfaces that made it challenging to navigate and complete purchases. However, in this particular example,               everything looks good to me. From my perspective, there is no need for any changes. However, I must mention that I am not a UI developer, so my opinion is             limited to what makes a good e-commerce website.
   4. Customer Loyalty. I think, this can be achieved by providing rewards and loyalty programs, and staying in touch with customers through email newsletters and           social media updates. Good example in our counrty [zalando.pl](https://www.zalando.pl/). But I think mentioned website from you has the same system.


  Overall, these factors are important for all e-commerce websites, not just for advertising purposes. Advertising was just used as an example.  
  

 ### Identify online KPIs
   In this paragraph, I would like to summarize/convert my answers to the previous question. 
   As I mentioned earlier, I believe that for this type of business, the most important indicator of success is revenue. Revenue, in turn, depends on the factors I        described in the previous question. Namely:

  1. Set up the connection between Google Search Console and Google Analytics 4 to recive information about CWV. Core Web Vitals are a set of metrics that measure how      users experience the speed, responsiveness, and visual stability of website. [web.dev](https://web.dev/learn-core-web-vitals/).          This will provide us with a better understanding of how the website is performing and allow us to identify any areas that need improvement.
  2. This point relates to the overall evaluation of the store, but I believe that tracking complaint and return forms can be set up. This way, the analytics                department can determine if there is an issue with the product, return process, or even a single user repeatedly filling out complaint forms, indicating that the      website support is not handling their job adequately. Keep in mind, this is just my personal overview on this process.
  3. This point partially relates to the answer in the previous question. In order to understand if the user is having any issues with making a purchase on the              website, for example, I would suggest tracking all error events on the site (red banners indicating incorrect information or any errors related to purchasing a        product). Tracking error events on the website can help identify which specific fields or areas may be difficult for users, providing valuable insights for the        development and UI teams. For instance, at our bank, we noticed that many users were encountering issues with entering their ZIP code (which is a common problem        in the UK), so we highlighted it as an area for improvement for our developers and UI team. They then implemented an automatic search for ZIP codes and added          tooltips at every step of the customer journey.
  4. While this topic may not directly relate to KPIs, it can still be helpful for analytics and marketing purposes. For instance, creating a remarketing audience for      Gmail, GDN, and other channels for people who have already completed a transaction can potentially help them make another purchase by offering incentives such as      free delivery or a discount.
  
 ### KPIs that will help to track the business objectives
   Regarding KPIs that will help to understand what going on, the most important:
   1. Purchases - available in GA4 by default. - How many users complited purchase.
   2. Avg. order value by user - tracks the average amount spent each time a customer places an order on a website.
   3. Conversion rate (including UI issues conversions rate and complaints forms) - calculated by simply taking the number of conversions and dividing that by the          number of total ad interactions that can be tracked to a conversion during the same time period.
   4. Cart abandonment rate - tracks users who add items to their shopping cart but then leave the website.
  
   ### List of tracking implementations that should be implemented for the specific eCommerce store
   Regarding tracking list that should be implemented, I don't what to create massive list of all available events, because it will be copy - paste from Google            documentation, so I will provide only once peace of code and all neccessary events for Ecommerce:
| Event Name | Explanation | 
| ---------- | ----------- | 
| view_item  | To measure how many times item details are viewed, send a view_item event whenever a user views an item’s details screen. |
| add_to_cart| To measure when someone adds merchandise to their shopping cart as a conversion, you need to set up the add_to_cart event your website. |
| remove_from_cart | To measure when a user removes an item from a cart. |
| begin_checkout  | Measure the first step in a checkout process by sending a begin_checkout event with one or more items defined with the relevant fields. A coupon can also be added at this stage to the entire order by adding it to the event or applied to a particular item by adding it to specific elements in the items array. | 
| add_shipping_info | When a user proceeds to the next step in the checkout process and adds shipping information. | 
| add_payment_info  | Send the add_payment_info event when a user submits their payment information. If applicable, include payment_type with this event for the chosen method of payment. |
| Purchase | Measure a purchase by sending a purchase event with one or more items defined with the relevant fields. The same apporach may be used for all events. Doceumentation in references section. |
| Refund | Measure a purchase by sending a purchase event with one or more items defined with the relevant fields |
  
| Event Name | Explanation | 
| ---------- | ----------- | 
| Purchase | Measure a purchase by sending a purchase event with one or more items defined with the relevant fields. The same apporach may be used for all events. Documentation in references section. |

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
  
  ### Referenсes 
- [Data Layer](https://developers.google.com/tag-platform/devguides/datalayer?hl=en)
- [GA4 Events](https://developers.google.com/analytics/devguides/collection/ga4/reference/events)
- [GA4 Objects schema](https://support.google.com/analytics/answer/10119380?hl=en)
- [Google E-Commerce example Website](https://enhancedecommerce.appspot.com/)


