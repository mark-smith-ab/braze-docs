---
nav_title: Logging Purchases
platform: Roku
page_order: 3
---
## Logging Purchases

Record in-app purchases so that you can track your revenue over time and across revenue sources, as well as segment your users by their lifetime value.

Braze supports purchases in multiple currencies. Purchases that you report in a currency other than USD will be shown in the dashboard in USD based on the exchange rate at the date they were reported.

Before implementation, be sure to review examples of the segmentation options afforded by Custom Events vs. Custom Attributes vs Purchase Events in our [Best Practices section][3].

To use this feature, add this method call after a successful purchase in your app:

```
m.Braze.logPurchase("PURCHASE_NAME", "CURRENCY_CODE", Double price, Integer quantity)
```

#### Adding Properties

You can add metadata about purchases by passing a properties dictionary with your purchase information.

Properties are defined as key-value pairs.  Keys are `String` objects and values can be `String` or `Integer`.

```
m.Braze.logPurchase("PURCHASE_NAME", "CURRENCY_CODE", Double price, Integer quantity, {"stringPropKey" : "stringPropValue", "intPropKey" : Integer intPropValue})
```

### REST API

You can also use our REST API to record purchases. Refer to the [user API documentation][2] for details.

[2]: {{ site.baseurl }}/developer_guide/rest_api/user_data/#user-data
[3]: {{ site.baseurl }}/developer_guide/platform_wide/analytics_overview/#user-data-collection
