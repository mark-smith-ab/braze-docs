---
nav_title: Integration
page_order: 0.1
search_rank: 3
platform: Web
---

# Content Cards for Web Integration

To toggle display of Content Cards through the Braze Web SDK, call:

[`appboy.display.toggleContentCards[();`](https://js.appboycdn.com/web-sdk/latest/doc/module-display.html#.toggleContentCards)


This will show the Content Cards if they are not shown, and hide them if they are. If no parameters are defined (null), all Content Cards will be shown in a fixed-position sidebar on the right-hand side of the page.

|Parameters | Description |
|---|---|
|`parentNode` | The HTML node to render the content cards into. If the parent node already has a Braze content cards view as a direct descendant, the existing content cards will be replaced. |
|`filterFunction` | A filter/sort function for cards displayed in this view. Invoked with the array of ab.Card objects, sorted by {pinned, date}. Expected to return an array of sorted ab.Card objects to render for this user. If omitted, all cards will be displayed. |

[See the JS docs](https://js.appboycdn.com/web-sdk/latest/doc/module-display.html#.toggleContentCards) for more information on toggling Content Cards.

## Other Methods to Note

|Method | Description | Link|
|---|---|---|
|`showContentCards`| Display the user's Content Cards. | [JS Docs for showContentCards](https://js.appboycdn.com/web-sdk/latest/doc/module-display.html#.showContentCards)|
|`hideContentCards`| Hide any Braze content cards currently showing. | [JS Docs for hideContentCards](https://js.appboycdn.com/web-sdk/latest/doc/module-display.html#.hideContentCards)
|`toggleContentCards`| Display the user's content cards. | [JS Docs for showContentCards](https://js.appboycdn.com/web-sdk/latest/doc/module-display.html#.toggleContentCards)
|`getCachedContentCards()`|Get all currently available cards from the last content cards refresh.| [JS Docs for getCachedContentCards](https://js.appboycdn.com/web-sdk/latest/doc/module-appboy.html#.getCachedContentCards)|
|`subscribeToContentCardsUpdates(subscriber)`| Subscribe to content cards updates. <br> The subscriber callback will be called whenever content cards are updated. |  [JS Docs for subscribeToContentCardsUpdates](https://js.appboycdn.com/web-sdk/latest/doc/module-appboy.html#.getCachedContentCards)|
