---
nav_title: Logging Custom Events
platform: Roku
page_order: 2
---
## Logging Custom Events

You can record custom events in Braze to learn more about your app's usage patterns and to segment your users by their actions on the dashboard.

You can use the following methods to track important user actions and custom events:

```
m.Braze.logEvent("YOUR_EVENT_NAME")
```

#### Adding Properties

You can add metadata about custom events by passing a properties dictionary with your custom event.

Properties are defined as key-value pairs.  Keys are `String` objects and values can be `String`, or `Integer`.

```
m.Braze.logEvent("YOUR_EVENT_NAME", {"stringPropKey" : "stringPropValue", "intPropKey" : Integer intPropValue})
```

[0]: {{ site.baseurl }}/developer_guide/platform_wide/analytics_overview/#user-data-collection
